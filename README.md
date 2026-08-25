# GameVerse

Trabalho avaliativo da disciplina de Desenvolvimento Web — IFCE Campus Aracati.

## Integrante

- João Pedro

## Tema

**Jogos** — o GameVerse é um portal fictício que reúne jogos indie de diferentes gêneros
(RPG, corrida, terror, luta, puzzle e estratégia) em uma vitrine única, com foco em
curadoria e descoberta. Todos os jogos apresentados são fictícios, criados especificamente
para este projeto.

## Descrição do Projeto

Site responsivo construído em **HTML5 e CSS3 puro**, sem frameworks CSS (Bootstrap,
Tailwind, etc.) e sem dependência de JavaScript. O projeto é composto por 3 páginas:

- **index.html** — Página inicial com seção de destaque (hero), grade de jogos em destaque
  e galeria de imagens com modal
- **sobre.html** — Sobre a plataforma e o desenvolvedor
- **contato.html** — Formulário de contato

## Como Executar o Projeto

Não há dependências nem build — é HTML/CSS estático. Basta:

1. Baixar ou clonar o repositório
2. Abrir o arquivo `index.html` diretamente no navegador

Ou, se preferir servir localmente (opcional):
```bash
npx serve .
```

## Mapa do Checklist Técnico

| Requisito | Onde está |
|---|---|
| Flexbox | `styles/base.css` — `header`, `nav ul`, `footer` \| `styles/components.css` — `form` |
| CSS Grid | `styles/layout.css` — `.cards-grid`, `.gallery-grid` |
| Media queries | `styles/layout.css` — breakpoints `@media (max-width: 900px)`, `@media (max-width: 600px)` e `@media (prefers-color-scheme: light)` |
| CSS Variables | `styles/base.css` — bloco `:root` (cores, espaçamento, tipografia) |
| Image modal | `styles/components.css` — `.modal` + `.modal-toggle:checked ~ .modal` (usado em `index.html`, seção Galeria) |
| Animations | `styles/animations.css` — `@keyframes surgir-de-baixo`, `@keyframes pulsar`, `@keyframes brilho-borda` |
| Backgrounds | `styles/layout.css` — `.hero` (gradientes radiais) \| `index.html` (inline) — capas dos cards com `linear-gradient` |
| CSS Units | uso de `rem`, `%`, `vh`, `vw`, `ch`, `clamp()` em `styles/base.css` e `styles/layout.css` |
| Pseudo-elements | `styles/base.css` — `.secao-titulo::after` \| `styles/components.css` — `.card-titulo::before` |
| Pseudo-classes | `styles/components.css` — `:hover` (cards/botões), `:focus-visible`, `:checked` (modal), `:invalid` (formulário) |
| Float | `sobre.html` — foto do desenvolvedor com `float: left`, texto contornando ao redor |
| Position + z-index | `styles/base.css` — `header { position: sticky }` \| `styles/components.css` — `.badge { position: absolute }`, `.modal { position: fixed }` |

## Fluxo de Colaboração (Trabalho Individual)

Este trabalho foi desenvolvido **individualmente**. Para simular um fluxo colaborativo real,
utilizei **duas contas GitHub próprias**, ambas pertencentes ao mesmo estudante (João Pedro):

- **[pedrosantos05-ib](https://github.com/pedrosantos05-ib)** — conta principal, dona do repositório
- **[IBliind](https://github.com/IBliind)** — conta secundária, simulando um segundo colaborador

O fluxo seguiu o modelo branch → commits → Pull Request → revisão → merge:

1. Commit inicial da estrutura do projeto feito pela conta principal (`pedrosantos05-ib`) na `main`
2. Criação da branch `feature/ajuste-galeria`, com commit de ajuste de estilo feito pela conta
   secundária (`IBliind`)
3. Abertura do Pull Request #1, com revisão e comentário de aprovação
4. Merge do Pull Request na `main`

**Pull Request de referência**: `#1 - style: aumenta espaçamento entre imagens da galeria`

Ambas as contas aparecem no histórico de commits e na lista de colaboradores do repositório.

## Uso de Inteligência Artificial Generativa

Foi utilizado o Claude (Anthropic) como ferramenta de apoio ao estudo durante o
desenvolvimento deste projeto, para:
- Explicar conceitos de CSS (Grid, pseudo-classes, a técnica de modal via `:checked`)
- Gerar a estrutura inicial do HTML/CSS a partir dos requisitos da atividade
- Auxiliar na configuração do fluxo de duas contas GitHub (SSH, branches, Pull Request)
- Revisar e depurar o código

Todo o código entregue foi revisado e é de conhecimento do estudante, que está apto a
explicá-lo e alterá-lo na apresentação técnica.

## Apresentação Técnica

**Tópico CSS escolhido para o deep dive**: CSS Grid — aplicado na `.cards-grid` (jogos em
destaque) e na `.gallery-grid` (galeria, com um item ocupando 2 colunas/linhas via
`grid-column: span 2` / `grid-row: span 2`), incluindo a adaptação responsiva por media
queries.
