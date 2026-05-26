# Projeto Grupo 7

Henrique | Joao Gabriel | Matheus | Paulo Henrique

---

## 📋 AVALIAÇÃO DO HTML - RESERVA DE PROJETORES

### 🎯 QUADRO DE AVALIAÇÃO GERAL

| **Critério** | **Pontuação** | **Status** | **Justificativa** |
|--------------|:-------------:|:---------:|---|
| **1. Tags Semânticas HTML5** | **6/10** | ⚠️ Parcial | Usa corretamente `<header>`, `<main>`, `<footer>`, `<section>`, `<aside>`; porém faltam estruturas mais robustas |
| **2. Estruturação de Formulários** | **4/10** | ❌ Crítico | Labels **não associados** aos inputs, faltam `name` e `id`, `action` vazio, estrutura desorganizada |
| **3. Código Limpo e Indentação** | **5/10** | ⚠️ Fraco | Indentação presente; excesso de linhas em branco desnecessárias; erros estruturais graves |
| **4. Ausência de "Div Soup"** | **9/10** | ✅ Excelente | Uso correto de tags semânticas; não abusa de `<div>` |
| **5. Estrutura Geral do Documento** | **3/10** | ❌ Crítico | Tabela com estrutura HTML quebrada; atributos vazios; falta `<nav>` |

### 📊 **NOTA FINAL: 5.4/10** + Ponto extra 5.0 = 9.4
### **CONCEITO: INSUFICIENTE** ❌

---

## 🔍 ANÁLISE DETALHADA POR CRITÉRIO

### **1️⃣ TAGS SEMÂNTICAS HTML5** - 6/10

#### ✅ Pontos Positivos:
- Uso correto de `<header>` (linhas 12-21)
- Uso correto de `<main>` (linhas 22-70)
- Uso correto de `<footer>` (linhas 72-76)
- Uso correto de `<section>` (linhas 23-28)
- Uso correto de `<aside>` (linhas 44-69)

#### ❌ Problemas Encontrados:

| Problema | Linha | Severidade | Correção |
|----------|:-----:|:----------:|----------|
| **Falta `<nav>`** | Geral | Alta | Adicionar menu de navegação se necessário |
| **`<h2>` dentro de `<aside>`** | 45-47 | Média | Rever hierarquia - `<h2>` deveria ser `<h3>` ou `<h4>` após `<main>` > `<section>` > `<h2>` |
| **Espaços excessivos em tags** | 13-15, 24-27 | Baixa | Remover quebras de linha desnecessárias dentro de tags |

---

### **2️⃣ ESTRUTURAÇÃO DE FORMULÁRIOS** - 4/10 ⚠️ **CRÍTICO**

#### ❌ PROBLEMAS GRAVES ENCONTRADOS:

**Problema 1: Labels não associados aos inputs**
- **Linhas afetadas:** 49-50, 52-53, 55-56, 58-59
- **Impacto:** Labels não funcionam, formulário inacessível
- **Requisito:** Todo `<label>` deve ter `for="id_correspondente"` e todo `<input>` deve ter `id` e `name`

**Problema 2: Atributo `for` vazio em todas as labels**
- **Linhas:** 49, 52, 55, 58
- **Impacto:** Labels não estão funcionais, não acessíveis
- **Solução:** Preencher com IDs válidos correspondentes aos inputs

**Problema 3: Inputs sem atributos `name`**
- **Linhas:** 50, 53, 56
- **Impacto:** Dados não serão enviados ao servidor quando o formulário for submetido
- **Solução:** Adicionar `name` em todos os campos de entrada

**Problema 4: Select sem atributo `name` e `id`**
- **Linhas:** 59-65
- **Impacto:** Select não será funcionário, dados não serão enviados
- **Solução:** Adicionar `name`, `id` e associar com `<label>`

**Problema 5: Formulário sem `method` e `action` definidos**
- **Linha:** 48
- **Impacto:** Formulário não sabe para onde enviar dados
- **Solução:** Definir `method="POST"` ou `GET` e `action` com URL válida

**Problema 6: Options com `value` vazio**
- **Linhas:** 60-62
- **Impacto:** Impossível distinguir qual opção foi selecionada
- **Solução:** Preencher `value` com valores significativos

#### ✅ Pontos Positivos:
- ✅ Usa tipos corretos de input (`type="text"`, `type="date"`, `type="time"`)
- ✅ Estrutura básica da tag `<form>` está presente
- ✅ `<button type="submit">` está correto

---

### **3️⃣ CÓDIGO LIMPO E INDENTAÇÃO** - 5/10

#### ✅ Pontos Positivos:
- Indentação básica presente e consistente (4 espaços)
- Estrutura hierárquica respeitada

#### ❌ Problemas Encontrados:

| Problema | Linhas | Severidade | Descrição |
|----------|:------:|:----------:|-----------|
| **Espaços em branco excessivos** | 19-20, 78-82 | Baixa | Múltiplas linhas vazias desnecessárias |
| **Quebras de linha desnecessárias** | 13-15, 24-27, 45-47 | Média | Títulos quebrados em múltiplas linhas |
| **Indentação incorreta em tabela** | 30-41 | Alta | `<thead>` e `<tbody>` mal organizados |
| **Espaçamento no formulário** | 67 | Baixa | Espaços em branco trailing desnecessários |

---

### **4️⃣ AUSÊNCIA DE "DIV SOUP"** - 9/10 ⭐

#### ✅ Excelente!
O código **não abusa de `<div>`**, usando corretamente tags semânticas:
- `<header>` em vez de `<div class="header">`
- `<main>` em vez de `<div class="main">`
- `<section>` em vez de `<div class="section">`
- `<aside>` em vez de `<div class="sidebar">`
- `<footer>` em vez de `<div class="footer">`

#### ⚠️ Sugestão de Melhoria:
- Considerar usar `<fieldset>` e `<legend>` para agrupar campos do formulário

---

### **5️⃣ ESTRUTURA GERAL DO DOCUMENTO** - 3/10 ❌

#### ❌ Problemas Críticos:

**Problema 1: Tabela com estrutura HTML quebrada**
- **Linhas:** 29-42
- **Severidade:** CRÍTICA
- **Impacto:** Semântica HTML violada, tabela não renderiza corretamente
- **Detalhes:**
  - `<thead>` vazio na linha 30
  - `<tbody>` contém `<th>` (deveria estar em `<thead>`)
  - `<th>` misturado com `<td>` na mesma linha
  - `</thead>` vem depois de `</tbody>` (ordem invertida)

**Problema 2: Falta `<nav>` se há navegação**
- **Severidade:** ALTA
- **Impacto:** Se houver menu, deve estar em `<nav>`
- **Solução:** Adicionar `<nav>` apropriadamente se necessário

---

## 📋 RESUMO DE PROBLEMAS CRÍTICOS

| ID | Severidade | Problema | Impacto |
|:--:|:----------:|----------|--------|
| 1 | 🔴 CRÍTICA | Labels sem associação aos inputs | Formulário não acessível, não funciona com leitores de tela |
| 2 | 🔴 CRÍTICA | Inputs sem `name` | Dados não serão enviados ao servidor |
| 3 | 🔴 CRÍTICA | Tabela com estrutura quebrada | Semântica HTML violada |
| 4 | 🟠 ALTA | `<form>` sem `method` e `action` | Não sabe onde enviar dados |
| 5 | 🟠 ALTA | Options com `value` vazio | Impossível distinguir as opções |
| 6 | 🟡 MÉDIA | Espaços em branco excessivos | Código desorganizado |

---

## ✅ RECOMENDAÇÕES PARA MELHORIA

### Prioridade 1 (Crítico - Fazer Imediatamente):
1. ✅ Adicionar `id` em todos os inputs
2. ✅ Preencher corretamente os atributos `for` das labels
3. ✅ Adicionar atributos `name` em todos os campos
4. ✅ Corrigir estrutura da tabela (thead/tbody)
5. ✅ Definir `method` e `action` no formulário

### Prioridade 2 (Alto - Fazer em Seguida):
6. ✅ Remover espaços em branco excessivos
7. ✅ Preenchimentos `value` corretos nas options
8. ✅ Usar `<fieldset>` e `<legend>` no formulário

### Prioridade 3 (Médio - Melhorias):
9. ✅ Adicionar `<nav>` se houver menu
10. ✅ Adicionar atributos `required` aos campos obrigatórios

---

## 🎓 CONCLUSÃO

O código apresenta uma **base estrutural razoável** com uso correto de tags semânticas, mas possui **problemas críticos na acessibilidade e funcionalidade do formulário** que devem ser corrigidos urgentemente. A principal deficiência é a **falta de associação entre labels e inputs**, o que torna o formulário inacessível e não funcional.

**Para melhorar a nota, o grupo deve priorizar:**
1. Associar corretamente labels e inputs
2. Adicionar atributos `name` em todos os campos
3. Corrigir a estrutura da tabela
