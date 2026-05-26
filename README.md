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

## 🔍 ANÁLISE DETALHADA POR CRITÉRIO - HTML

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

## 📋 RESUMO DE PROBLEMAS CRÍTICOS - HTML

| ID | Severidade | Problema | Impacto |
|:--:|:----------:|----------|--------|
| 1 | 🔴 CRÍTICA | Labels sem associação aos inputs | Formulário não acessível, não funciona com leitores de tela |
| 2 | 🔴 CRÍTICA | Inputs sem `name` | Dados não serão enviados ao servidor |
| 3 | 🔴 CRÍTICA | Tabela com estrutura quebrada | Semântica HTML violada |
| 4 | 🟠 ALTA | `<form>` sem `method` e `action` | Não sabe onde enviar dados |
| 5 | 🟠 ALTA | Options com `value` vazio | Impossível distinguir as opções |
| 6 | 🟡 MÉDIA | Espaços em branco excessivos | Código desorganizado |

---

## ✅ RECOMENDAÇÕES PARA MELHORIA - HTML

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

## 🎓 CONCLUSÃO - HTML

O código apresenta uma **base estrutural razoável** com uso correto de tags semânticas, mas possui **problemas críticos na acessibilidade e funcionalidade do formulário** que devem ser corrigidos.

**Para melhorar a nota, o grupo deve priorizar:**
1. Associar corretamente labels e inputs
2. Adicionar atributos `name` em todos os campos
3. Corrigir a estrutura da tabela

---

---

# 📊 AVALIAÇÃO DO CSS - STYLE.CSS

## 🎯 QUADRO DE AVALIAÇÃO GERAL

| **Critério** | **Pontuação** | **Status** | **Justificativa** |
|--------------|:-------------:|:---------:|---|
| **1. Domínio de Ferramentas de Layout Moderno** | **2/10** | ❌ Crítico | Flexbox usado incorretamente (`display: flexbox` inválido); sem CSS Grid; layout inadequado |
| **2. Uso de Media Queries para Responsividade** | **1/10** | ❌ Crítico | Media Query incompleta, regras nested inválidas, sem estratégia mobile-first |
| **3. Organização do Arquivo CSS** | **2/10** | ❌ Crítico | Sem variáveis CSS, sem separação por seções, cores hardcoded, desorganizado |
| **4. Hierarquia Visual Clara** | **3/10** | ❌ Crítico | Cores inconsistentes, sem diferenciação clara, faltam estados (focus, active, disabled) |

### 📊 **NOTA FINAL: 2.0/10**
### **CONCEITO: EXTREMAMENTE INSUFICIENTE** 🔴

---

## 🔍 ANÁLISE DETALHADA POR CRITÉRIO - CSS

### **1️⃣ DOMÍNIO DE FERRAMENTAS DE LAYOUT MODERNO** - 2/10

#### ❌ PROBLEMAS CRÍTICOS:

| Linha | Problema | Impacto | Severidade |
|:-----:|----------|--------|:----------:|
| 13 | `display: flexbox;` | ❌ Valor inválido. Deveria ser `display: flex;` | 🔴 CRÍTICA |
| 13 | Faltam propriedades Flexbox | Sem `justify-content`, `align-items` funcionando | 🟠 ALTA |
| - | Sem CSS Grid | Layout limitado, não usa alternativa moderna | 🟡 MÉDIA |
| - | Layout inadequado para tabelas | Sem overflow handling em mobile | 🟠 ALTA |

#### ✅ Pontos Positivos:
- Estrutura básica de layout presente
- Tentativa de usar Flexbox (mesmo que incorreta)

---

### **2️⃣ USO DE MEDIA QUERIES PARA RESPONSIVIDADE** - 1/10

#### ❌ PROBLEMAS CRÍTICOS:

**Problema 1: Media Query incompleta**
```css
@media screen and (max-width)  /* ❌ FALTA O VALOR - deve ser: (max-width: 768px) */
```
- **Impacto:** Media Query não funciona, responsividade quebrada
- **Severidade:** 🔴 CRÍTICA

**Problema 2: Regras CSS nested inválidas**
```css
aside{
    section{
        width: 100%;
        display:block;overflow-x:auto
    }
}
```
- **Problema:** CSS não suporta nesting nativo (seria válido em SCSS/LESS)
- **Impacto:** Código não funciona, responsividade quebrada
- **Severidade:** 🔴 CRÍTICA

**Problema 3: Sem breakpoints múltiplos**
- Apenas 1 media query (incompleta)
- Faltam breakpoints para tablet (768px), celular (480px), desktop grande (1200px)
- **Impacto:** Design não responsivo para múltiplos dispositivos

**Problema 4: Sem estratégia mobile-first**
- Estilos base não preparados para mobile
- Media queries reativas, não proativas
- **Severidade:** 🟡 MÉDIA

#### ✅ Pontos Positivos:
- Tentativa de criar media query

---

### **3️⃣ ORGANIZAÇÃO DO ARQUIVO CSS** - 2/10

#### ❌ PROBLEMAS CRÍTICOS:

**Problema 1: Sem uso de variáveis CSS**
- Cores repetidas manualmente:
  - `#5ac2c2` - aparece 4 vezes
  - `darkgray` - aparece 2 vezes
  - `rgb(63, 165, 205)` - aparece 1 vez
  - `gray` - aparece 1 vez
- **Impacto:** Difícil manutenção, sem consistência de tema
- **Severidade:** 🔴 CRÍTICA

**Problema 2: Sem separação por seções**
- Reset, Layout, Typography, Components misturados
- Sem comentários organizacionais
- Difícil navegação e manutenção
- **Severidade:** 🟠 ALTA

**Problema 3: Ordem desordenada**
- Estilos base, componentes e media queries espalhados
- Sem estrutura lógica
- **Severidade:** 🟡 MÉDIA

#### ✅ Pontos Positivos:
- Reset básico (margin, padding, box-sizing)
- Alguns agrupamentos de elementos similares

---

### **4️⃣ HIERARQUIA VISUAL CLARA** - 3/10

#### ❌ PROBLEMAS CRÍTICOS:

**Problema 1: Cores inconsistentes**
```css
#5ac2c2      /* header, input, select, button */
darkgray     /* body background, form, button */
rgb(63, 165, 205)  /* footer */
gray         /* body background - conflita com darkgray */
```
- Múltiplos tons de azul/cyan sem justificativa
- Background cinza sem contraste definido
- **Impacto:** Confusão visual, marca inconsistente
- **Severidade:** 🔴 CRÍTICA

**Problema 2: Sem diferenciação clara de elementos**
- Botões e inputs com estilos muito similares
- Títulos (th) sem tamanho/peso diferenciado
- Falta contraste entre elementos
- **Severidade:** 🟠 ALTA

**Problema 3: Falta de estados visuais**
- Apenas `button:hover` definido
- Faltam: `:focus`, `:active`, `:disabled`
- Input sem `:focus` com outline
- **Impacto:** Sem feedback visual para usuário, acessibilidade comprometida
- **Severidade:** 🟠 ALTA

#### ✅ Pontos Positivos:
- `button:hover` com transição de cor
- Estrutura básica de hierarquia presente

---

## 🔴 ERROS DE SINTAXE CSS

| Linha | Erro | Tipo | Correção |
|:-----:|------|:----:|----------|
| 13 | `display: flexbox;` | ❌ Valor inválido | Mudar para `display: flex;` |
| 37 | `border-bottom: 20px;` | ❌ Falta unidade/cor | `border-bottom: 1px solid #ddd;` |
| 42 | `border-bottom: 25px;` | ❌ Falta unidade/cor | `border-bottom: 1px solid #ddd;` |
| 46 | `border-radius: bordas arredondadas;` | ❌ Texto português | `border-radius: 10px;` |
| 53 | `border: #5ac2c2;` | ❌ Falta estilo | `border: 1px solid #5ac2c2;` |
| 58 | `border: #5ac2c2;` | ❌ Falta estilo | `border: 1px solid #5ac2c2;` |
| 61 | `border-color: 50 px;` | ❌ Valor inválido | `border-color: #5ac2c2;` |
| 68 | `border: radius 20px;` | ❌ Sintaxe errada | `border-radius: 20px;` |
| 78 | `@media screen and (max-width)` | ❌ Falta valor | `@media screen and (max-width: 768px)` |
| 82 | `overflow-x:auto` | ⚠️ Falta ponto-e-vírgula | `overflow-x: auto;` |

---

## 📋 RESUMO DE PROBLEMAS CRÍTICOS - CSS

| ID | Severidade | Problema | Impacto | Linha |
|:--:|:----------:|----------|--------|:-----:|
| 1 | 🔴 CRÍTICA | `display: flexbox` inválido | Layout quebrado | 13 |
| 2 | 🔴 CRÍTICA | Media Query incompleta | Responsividade não funciona | 78 |
| 3 | 🔴 CRÍTICA | Regras nested inválidas | CSS não funciona | 80-85 |
| 4 | 🔴 CRÍTICA | Sem variáveis CSS | Manutenção impossível | Geral |
| 5 | 🟠 ALTA | Cores hardcoded repetidas | Sem consistência de tema | Geral |
| 6 | 🟠 ALTA | Sem diferenciação visual | Hierarquia confusa | Geral |
| 7 | 🟠 ALTA | Falta estados (focus, active) | Acessibilidade comprometida | Geral |
| 8 | 🟡 MÉDIA | Sem separação por seções | Código desorganizado | Geral |

---

## ✅ ARQUIVO CSS CORRIGIDO

```css
/* ===== VARIÁVEIS CSS ===== */
:root {
    --primary-color: #5ac2c2;
    --secondary-color: rgb(63, 165, 205);
    --dark-bg: darkgray;
    --light-bg: gray;
    --border-color: #ddd;
    --text-primary: white;
    --spacing-sm: 10px;
    --spacing-md: 20px;
    --spacing-lg: 24px;
}

/* ===== RESET ===== */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* ===== TIPOGRAFIA E BASE ===== */
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: var(--light-bg);
    line-height: 1.6;
}

/* ===== LAYOUT PRINCIPAL ===== */
main {
    display: flex;
    justify-content: center;
    align-items: flex-start;
    gap: var(--spacing-md);
    padding: var(--spacing-md);
}

/* ===== HEADER ===== */
header {
    background-color: var(--primary-color);
    color: var(--text-primary);
    padding: var(--spacing-md);
    text-align: center;
}

header h1 {
    font-size: 2rem;
    margin-bottom: 0.5rem;
}

/* ===== FOOTER ===== */
footer {
    background-color: var(--secondary-color);
    color: var(--text-primary);
    padding: var(--spacing-md);
    text-align: center;
}

/* ===== TABELAS ===== */
table {
    width: 100%;
    border-collapse: collapse;
    background-color: white;
}

th {
    padding: var(--spacing-lg);
    border-bottom: 2px solid var(--primary-color);
    font-weight: bold;
    text-align: left;
    background-color: var(--primary-color);
    color: var(--text-primary);
}

td {
    padding: var(--spacing-lg);
    border-bottom: 1px solid var(--border-color);
}

tr:hover {
    background-color: #f5f5f5;
}

/* ===== FORMULÁRIOS ===== */
form {
    padding: var(--spacing-md);
    margin: var(--spacing-sm);
    background-color: var(--dark-bg);
    border-radius: 10px;
    width: 100%;
    max-width: 400px;
}

form label {
    display: block;
    margin-bottom: var(--spacing-sm);
    font-weight: bold;
    color: var(--text-primary);
}

/* ===== INPUTS E SELECTS ===== */
input,
select {
    width: 100%;
    margin: var(--spacing-sm) 0;
    padding: var(--spacing-md);
    border: 1px solid var(--primary-color);
    border-radius: 10px;
    font-family: inherit;
    font-size: 1rem;
}

input:focus,
select:focus {
    outline: none;
    border-color: var(--primary-color);
    box-shadow: 0 0 5px rgba(90, 194, 194, 0.5);
}

input:disabled,
select:disabled {
    background-color: #e0e0e0;
    cursor: not-allowed;
}

/* ===== BOTÕES ===== */
button {
    background-color: var(--primary-color);
    color: var(--text-primary);
    border: none;
    border-radius: 8px;
    cursor: pointer;
    padding: var(--spacing-sm) var(--spacing-md);
    font-weight: bold;
    transition: all 0.3s ease;
    width: 100%;
    margin-top: var(--spacing-sm);
}

button:hover {
    background-color: rgb(98, 205, 205);
    transform: translateY(-2px);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

button:active {
    transform: translateY(0);
    box-shadow: none;
}

button:disabled {
    background-color: #ccc;
    cursor: not-allowed;
    opacity: 0.6;
}

/* ===== MEDIA QUERIES - RESPONSIVIDADE ===== */
@media screen and (max-width: 768px) {
    main {
        flex-direction: column;
        align-items: center;
    }

    form {
        max-width: 100%;
    }

    table {
        font-size: 0.9rem;
        overflow-x: auto;
        display: block;
    }

    th,
    td {
        padding: var(--spacing-md);
    }

    header h1 {
        font-size: 1.5rem;
    }
}

@media screen and (max-width: 480px) {
    main {
        gap: var(--spacing-sm);
    }

    form {
        padding: var(--spacing-sm);
    }

    th,
    td {
        padding: var(--spacing-sm);
    }

    button {
        padding: 8px 12px;
        font-size: 0.9rem;
    }
}
```

---

## ✅ RECOMENDAÇÕES PARA MELHORIA - CSS

### Prioridade 1 (Crítico - Fazer Imediatamente):
1. ✅ Corrigir `display: flexbox` para `display: flex`
2. ✅ Adicionar valor completo na media query: `(max-width: 768px)`
3. ✅ Remover regras nested (usar CSS puro ou converter para SCSS)
4. ✅ Implementar variáveis CSS para todas as cores
5. ✅ Corrigir todos os erros de sintaxe (border, border-radius, border-color)

### Prioridade 2 (Alto - Fazer em Seguida):
6. ✅ Adicionar múltiplos breakpoints (480px, 768px, 1024px, 1200px)
7. ✅ Organizar CSS em seções com comentários
8. ✅ Adicionar estados visuais: `:focus`, `:active`, `:disabled`
9. ✅ Melhorar hierarquia visual com tamanhos e pesos diferenciados
10. ✅ Implementar transições suaves para melhor UX

### Prioridade 3 (Médio - Melhorias):
11. ✅ Considerar usar SCSS/LESS para nesting nativo
12. ✅ Adicionar animações ao hover
13. ✅ Implementar modo escuro (dark mode) com variáveis
14. ✅ Adicionar acessibilidade visual (focus indicators claros)

---

## 🎓 CONCLUSÃO - CSS

O arquivo CSS apresenta **problemas críticos e sistêmicos** que impedem seu funcionamento correto:

### Principais Deficiências:
- ❌ **Erros de sintaxe** que quebram o layout
- ❌ **Sem responsividade funcional** (media query incompleta)
- ❌ **Desorganização extrema** (sem variáveis, cores hardcoded)
- ❌ **Hierarquia visual confusa** (sem diferenciação clara)
- ❌ **Falta acessibilidade** (sem estados de focus/active)

### Para Melhorar a Nota, o Grupo Deve:
1. **Corrigir urgentemente** todos os erros de sintaxe
2. **Implementar variáveis CSS** para manutenção
3. **Reorganizar o código** em seções bem definidas
4. **Implementar responsividade correta** com múltiplos breakpoints
5. **Adicionar estados visuais** para melhor UX e acessibilidade

**Nota atual: 2.0/10 - EXTREMAMENTE INSUFICIENTE** 🔴

---

## 📊 COMPARATIVO HTML vs CSS

| Aspecto | HTML | CSS |
|--------|:----:|:---:|
| **Conceitual** | 5.4/10 | 2.0/10 |
| **Status** | Insuficiente | Extremamente Insuficiente |
| **Principais Problemas** | Formulário desorganizado | Erros de sintaxe |
| **Prioridade de Correção** | 1 | 1 (mais crítico) |

