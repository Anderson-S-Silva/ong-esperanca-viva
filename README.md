# 🤝 ONG Esperança Viva - Plataforma Web HTML5 Semântica

Plataforma web institucional desenvolvida para a **ONG Esperança Viva**, focada na captação de voluntários, divulgação de projetos sociais e transparência de dados. O projeto foi construído com foco rigoroso em **semântica HTML5**, **acessibilidade digital (WCAG/eMAG)**, **validações de formulário** e **organização arquitetural de diretórios**.

---

## 📌 Sumário
- [Visão Geral do Desafio](#-visão-geral-do-desafio)
- [Arquitetura de Pastas](#-arquitetura-de-pastas)
- [Páginas e Estrutura Semântica](#-páginas-e-estrutura-semântica)
- [Acessibilidade e Usabilidade](#-acessibilidade-e-usabilidade)
- [Validações e Máscaras de Entrada](#-validações-e-máscaras-de-entrada)
- [Conformidade W3C](#-conformidade-w3c)
- [Como Executar o Projeto](#-como-executar-o-projeto)

---

## 🎯 Visão Geral do Desafio

As organizações do terceiro setor dependem de plataformas digitais claras para garantir credibilidade institucional e atrair doadores e voluntários. Este projeto resolve essa demanda ao entregar:
1. **Página Inicial (`index.html`)**: Apresentação da missão, pilares institucionais, mídia acessível e canais de contato.
2. **Página de Projetos (`projetos.html`)**: Exposição detalhada das frentes de atuação (`<article>`) e chamadas para ação (CTA).
3. **Página de Engajamento (`cadastro.html`)**: Formulário interativo com agrupamento lógico (`<fieldset>`), validações nativas e máscaras dinâmicas (CPF, Telefone, CEP).

---

## 📂 Arquitetura de Ficheiros

```text
ONG-ESPERANCA-VIVA/
│
├── assets/
│   ├── css/
│   │   └── style.css                   # Folha de estilos unificada e responsiva
│   └── img/
│       ├── favicon.svg                 # Ícone do site para a aba do navegador
│       ├── logo.svg                    # Logótipo vetorial institucional
│       ├── projeto-futuro-brilhante.jpg # Imagem do Projeto Futuro Brilhante
│       ├── projeto-gerando-autonomia.jpg# Imagem do Projeto Gerando Autonomia
│       ├── projeto-prato-cheio.jpg     # Imagem do Projeto Prato Cheio
│       └── voluntarios-acao.jpeg       # Imagem principal da seção Hero
│
├── cadastro.html                       # Formulário de registo de voluntários
├── index.html                          # Página inicial (Landing Page)
├── projetos.html                       # Apresentação das iniciativas e relatórios
├── relatorio-impacto.html              # Documento interativo em layout A4 para PDF
└── README.md                           # Documentação do projeto


## 🌐 Páginas e Estrutura Semântica

A aplicação respeita a hierarquia de cabeçalhos (`<h1>` único dentro do `<main>`, seguido por `<h2>` para seções e `<h3>` para subitens/cartões) e utiliza tags de seccionamento semântico do HTML5:

| Página | Estrutura Principal Utilizada | Objetivo |
| :--- | :--- | :--- |
| `index.html` | `<header>`, `<nav>`, `<main>`, `<section>`, `<figure>`, `<aside>`, `<address>`, `<footer>` | Apresentar a ONG, história, pilares e dados institucionais de contato. |
| `projetos.html` | `<main>`, `<section>`, `<article>`, `<figure>`, `<figcaption>` | Detalhar os projetos sociais de forma isolada e orientar doações. |
| `cadastro.html` | `<main>`, `<form>`, `<fieldset>`, `<legend>`, `<label>`, `<input>`, `<select>` | Capturar dados de novos colaboradores com alta integridade. |

---

## ♿ Acessibilidade e Usabilidade

O projeto atende aos padrões e recomendações de acessibilidade da web (WCAG 2.1):

- **Navegação por Teclado:** Incluído o link de salto rápido (`.sr-only`) `<a href="#conteudo-principal">` no topo das páginas.
- **Leitores de Tela:** Utilização dos atributos ARIA (`aria-label`, `aria-labelledby`, `aria-describedby` e `aria-current="page"`).
- **Mídia Acessível:** Todas as imagens possuem o atributo `alt` detalhado e descritivo, além de agrupamento via `<figure>` e `<figcaption>`.
- **Hierarquia de Títulos sem Saltos:** Transição lógica de `<h1>` para `<h2>` e `<h3>`, permitindo a montagem correta da árvore de navegação por leitores de tela.

---

## 🔒 Validações e Máscaras de Entrada

A página `cadastro.html` implementa uma camada dupla de validação para garantir a integridade dos dados coletados:

### 1. Validações Nativas HTML5
- Atributos `required` para impedir submissão de campos nulos.
- Atributos `minlength` e `maxlength` ajustados por campo.
- Atributo `pattern` configurado com Expressões Regulares (Regex) para validação no cliente (*client-side*):
  - **CPF:** `pattern="\d{3}\.\d{3}\.\d{3}-\d{2}"`
  - **Telefone:** `pattern="\(\d{2}\) \d{4,5}-\d{4}"`
  - **CEP:** `pattern="\d{5}-\d{3}"`

### 2. Máscaras Dinâmicas (JavaScript Vanilla)
Script leve que formata automaticamente a digitação do usuário em tempo real para os campos de **CPF** (`000.000.000-00`), **Telefone** (`(00) 00000-0000`) e **CEP** (`00000-000`), evitando erros de preenchimento.

---

## ✅ Conformidade W3C

O código-fonte de todas as páginas HTML5 foi submetido e validado junto ao [W3C Markup Validation Service](https://validator.w3.org/), garantindo:
- Zero erros de sintaxe ou abertura/fechamento de tags.
- Ausência de atributos depreciados.
- Total conformidade com as diretrizes do HTML5.

---

## 🚀 Como Executar o Projeto

1. Clone este repositório:
   ```bash
   git clone [https://github.com/SEU-USUARIO/ong-esperanca-viva.git](https://github.com/SEU-USUARIO/ong-esperanca-viva.git)

Abra o arquivo index.html em seu navegador de preferência (ou utilize a extensão Live Server no VS Code).