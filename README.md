# Catálogo Interativo de Jogos

Aplicação web desenvolvida para a disciplina de **Desenvolvimento Front-End Para Web**, com foco em manipulação dinâmica do DOM utilizando HTML5, CSS3 e JavaScript puro (Vanilla JS).
## Acesse o projeto

🌐 **[GAMEVERSE — Catálogo Interativo de Jogos](https://henriquepontesduarte13013-ctrl.github.io/projeto-integrador-frontend-henrique-duarte/)**

## Acesse o projeto

🌐 **[GAMEVERSE — Catálogo Interativo de Jogos](https://henriquepontesduarte13013-ctrl.github.io/projeto-integrador-frontend-henrique-duarte/)**

## Funcionalidades

- **Catálogo com 30 jogos** em 8 categorias: Ação e Aventura, Battle Royale, Esportes e Corrida, Mundo Aberto e Sandbox, RPG, FPS e MOBA, Estratégia e Simulação, e Plataforma, Luta e Terror.
- **Pesquisa por nome:** atualiza a cada tecla, sem diferenciar maiúsculas/minúsculas nem acentos.
- **Filtro por categoria:** chips e menu *Categorias* (gerados a partir dos dados em `js/catalogo.js`); combina com a pesquisa.
- **Favoritos:** favoritar/desfavoritar nos cards, lista na seção Favoritos com opção de remover, persistência em `localStorage` (chave `jogosFavoritos`) e *Event Delegation*.
- **SVG:** sprite inline de ícones (`<symbol>`/`<use>`), logo, favicon e uma ilustração original provisória (League of Legends). As demais capas são imagens reais locais (ver *Capas dos jogos*).
- **Canvas:** gráfico de barras horizontais "Favoritos por categoria" (todas as categorias, inclusive as com zero favoritos), redesenhado a cada alteração e ao redimensionar a tela, com alternativa em texto para leitores de tela.
- **Vídeo de destaque:** player `<video>` com legendas (`<track>`) e aviso de fallback quando o arquivo não existe.
- **Estados vazios, responsividade e acessibilidade** (ARIA, `aria-live`, foco visível).

## Tecnologias e Conceitos Aplicados

- **HTML5 Semântico:** `<header>`, `<main>`, `<section>`, `<article>`, `<figure>`, `<video>`, `<canvas>` e atributos `data-*`.
- **CSS3:** variáveis em `:root`, Flexbox, Grid, tema Dark Purple e media queries.
- **JavaScript (ES6+):** manipulação do DOM sem `innerHTML`, `CustomEvent`, `ResizeObserver`, API Canvas 2D e `localStorage`.

## Estrutura de Arquivos

```text
catalogo-jogos-dom/
├── index.html          # Estrutura semântica e sprite SVG
├── css/
│   ├── reset.css       # Reset (box-sizing: border-box)
│   └── style.css       # Variáveis, tema Dark Purple e componentes
├── js/
│   ├── main.js         # Inicialização, menu, dropdown e fallback do vídeo
│   ├── catalogo.js     # Dados (30 jogos, 8 categorias), pesquisa, filtros e favoritos
│   └── graficos.js     # Gráfico de barras em Canvas
└── assets/
    ├── images/         # 30 capas (capa-*.jpg / .svg) e pôster do vídeo
    ├── icons/          # Favicon
    ├── captions/       # Legendas WebVTT
    └── videos/         # Coloque aqui destaque.mp4 / destaque.webm
```

## Capas dos jogos: fontes e direitos de uso

As capas ficam salvas localmente em `assets/images/` (a página não carrega imagens de outros sites). Todas as proporções são preservadas: cada card usa uma moldura 2:3 com `object-fit: contain`, sem distorção nem corte.

**Aviso importante sobre direitos:** as capas dos jogos são obras protegidas por direitos autorais dos respectivos desenvolvedoras/publicadoras (Valve, Nintendo, Riot Games, Electronic Arts, Sony, Capcom, etc.) e **não são de uso livre**. Elas aparecem aqui somente para identificar cada jogo, em um **projeto acadêmico sem fins lucrativos**. As imagens da Steam são arte promocional de loja, e as da Wikipédia estão hospedadas lá sob alegação de *fair use* (válida no contexto da enciclopédia, sem garantia de reutilização livre). Os termos de uso/licenças de cada fonte não foram revistos juridicamente. Antes de qualquer publicação além da avaliação, é necessário obter permissão dos titulares ou substituir as imagens (por exemplo, por arte de *press kit* com licença explícita). Os titulares podem solicitar a remoção a qualquer momento.

| Jogo | Origem | Fonte | Arquivo |
|---|---|---|---|
| Brawl Stars | App Store (ícone oficial do app, Supercell Oy) | [App Store](https://apps.apple.com/us/app/brawl-stars/id1229016807) | `capa-brawl-stars.jpg` |
| Free Fire | Google Play (ícone oficial do app, Garena; arte temática de evento) | [Google Play](https://play.google.com/store/apps/details?id=com.dts.freefireth) | `capa-free-fire.png` |
| EA Sports FC | Steam (capa vertical oficial da loja) | [Página na Steam](https://store.steampowered.com/app/2669320/) · [imagem](https://cdn.cloudflare.steamstatic.com/steam/apps/2669320/library_600x900.jpg) | `capa-ea-sports-fc.jpg` |
| God of War Ragnarök | Steam (capa vertical oficial da loja) | [Página na Steam](https://store.steampowered.com/app/2322010/) · [imagem](https://cdn.cloudflare.steamstatic.com/steam/apps/2322010/library_600x900.jpg) | `capa-god-of-war-ragnarok.jpg` |
| The Legend of Zelda: Breath of the Wild | Wikipédia (EN), imagem de capa do artigo; arquivo marcado como *fair use* (Nintendo) | [Página do arquivo](https://en.wikipedia.org/wiki/File:The_Legend_of_Zelda_Breath_of_the_Wild.jpg) | `capa-zelda-breath-of-the-wild.jpg` |
| Fortnite | Epic Games Store (arte vertical oficial de divulgação do Fortnite Battle Royale, edição temática de temporada) | [Epic Games Store](https://store.epicgames.com/en-US/p/fortnite) | `capa-fortnite.jpg` |
| PUBG: Battlegrounds | Steam (capa vertical oficial da loja) | [Página na Steam](https://store.steampowered.com/app/578080/) · [imagem](https://cdn.cloudflare.steamstatic.com/steam/apps/578080/library_600x900.jpg) | `capa-pubg-battlegrounds.jpg` |
| Apex Legends | Steam (capa vertical oficial da loja) | [Página na Steam](https://store.steampowered.com/app/1172470/) · [imagem](https://cdn.cloudflare.steamstatic.com/steam/apps/1172470/library_600x900.jpg) | `capa-apex-legends.jpg` |
| Rocket League | Steam (capa vertical oficial da loja) | [Página na Steam](https://store.steampowered.com/app/252950/) · [imagem](https://cdn.cloudflare.steamstatic.com/steam/apps/252950/library_600x900.jpg) | `capa-rocket-league.jpg` |
| Forza Horizon 5 | Steam (capa vertical oficial da loja) | [Página na Steam](https://store.steampowered.com/app/1551360/) · [imagem](https://cdn.cloudflare.steamstatic.com/steam/apps/1551360/library_600x900.jpg) | `capa-forza-horizon-5.jpg` |
| Mario Kart 8 Deluxe | Loja oficial da Nintendo (imagem de divulgação da página do produto, formato horizontal) | [Nintendo Store](https://www.nintendo.com/us/store/products/mario-kart-8-deluxe-switch/) | `capa-mario-kart-8-deluxe.jpg` |
| GTA V | Steam (capa vertical oficial da loja) | [Página na Steam](https://store.steampowered.com/app/271590/) · [imagem](https://cdn.cloudflare.steamstatic.com/steam/apps/271590/library_600x900.jpg) | `capa-gta-v.jpg` |
| Minecraft | App Store (ícone oficial do app Minecraft, Mojang AB) | [App Store](https://apps.apple.com/us/app/minecraft-play-with-friends/id479516143) | `capa-minecraft.jpg` |
| Terraria | Steam (capa vertical oficial da loja) | [Página na Steam](https://store.steampowered.com/app/105600/) · [imagem](https://cdn.cloudflare.steamstatic.com/steam/apps/105600/library_600x900.jpg) | `capa-terraria.jpg` |
| Genshin Impact | App Store (ícone oficial do app, Cognosphere/HoYoverse) | [App Store](https://apps.apple.com/us/app/genshin-impact/id1517783697) | `capa-genshin-impact.jpg` |
| Elden Ring | Steam (capa vertical oficial da loja) | [Página na Steam](https://store.steampowered.com/app/1245620/) · [imagem](https://cdn.cloudflare.steamstatic.com/steam/apps/1245620/library_600x900.jpg) | `capa-elden-ring.jpg` |
| The Witcher 3 | Steam (capa vertical oficial da loja) | [Página na Steam](https://store.steampowered.com/app/292030/) · [imagem](https://cdn.cloudflare.steamstatic.com/steam/apps/292030/library_600x900.jpg) | `capa-the-witcher-3.jpg` |
| Valorant | Wikipédia (EN), imagem de capa do artigo; arquivo marcado como *fair use* (Riot Games) | [Página do arquivo](https://en.wikipedia.org/wiki/File:Valorant_cover.jpg) | `capa-valorant.jpg` |
| Counter-Strike 2 | Steam (capa vertical oficial da loja) | [Página na Steam](https://store.steampowered.com/app/730/) · [imagem](https://cdn.cloudflare.steamstatic.com/steam/apps/730/library_600x900.jpg) | `capa-counter-strike-2.jpg` |
| League of Legends | **Sem capa oficial incluída** — ilustração SVG original do projeto (provisória) | — | `capa-league-of-legends.svg` |
| Dota 2 | Steam (capa vertical oficial da loja) | [Página na Steam](https://store.steampowered.com/app/570/) · [imagem](https://cdn.cloudflare.steamstatic.com/steam/apps/570/library_600x900.jpg) | `capa-dota-2.jpg` |
| Clash of Clans | App Store (ícone oficial do app, Supercell Oy) | [App Store](https://apps.apple.com/us/app/clash-of-clans/id529479190) | `capa-clash-of-clans.jpg` |
| Civilization VI | Steam (capa vertical oficial da loja) | [Página na Steam](https://store.steampowered.com/app/289070/) · [imagem](https://cdn.cloudflare.steamstatic.com/steam/apps/289070/library_600x900.jpg) | `capa-civilization-vi.jpg` |
| The Sims 4 | Steam (capa vertical oficial da loja) | [Página na Steam](https://store.steampowered.com/app/1222670/) · [imagem](https://cdn.cloudflare.steamstatic.com/steam/apps/1222670/library_600x900.jpg) | `capa-the-sims-4.jpg` |
| Stardew Valley | Steam (capa vertical oficial da loja) | [Página na Steam](https://store.steampowered.com/app/413150/) · [imagem](https://cdn.cloudflare.steamstatic.com/steam/apps/413150/library_600x900.jpg) | `capa-stardew-valley.jpg` |
| Hollow Knight | Steam (capa vertical oficial da loja) | [Página na Steam](https://store.steampowered.com/app/367520/) · [imagem](https://cdn.cloudflare.steamstatic.com/steam/apps/367520/library_600x900.jpg) | `capa-hollow-knight.jpg` |
| Super Mario Odyssey | Wikipédia (EN), imagem de capa do artigo; arquivo marcado como *fair use* (Nintendo) | [Página do arquivo](https://en.wikipedia.org/wiki/File:Super_Mario_Odyssey.jpg) | `capa-super-mario-odyssey.jpg` |
| Street Fighter 6 | Steam (capa vertical oficial da loja) | [Página na Steam](https://store.steampowered.com/app/1364780/) · [imagem](https://cdn.cloudflare.steamstatic.com/steam/apps/1364780/library_600x900.jpg) | `capa-street-fighter-6.jpg` |
| Among Us | Steam (capa vertical oficial da loja) | [Página na Steam](https://store.steampowered.com/app/945360/) · [imagem](https://cdn.cloudflare.steamstatic.com/steam/apps/945360/library_600x900.jpg) | `capa-among-us.jpg` |
| Resident Evil 4 | Steam (capa vertical oficial da loja) | [Página na Steam](https://store.steampowered.com/app/2050650/) · [imagem](https://cdn.cloudflare.steamstatic.com/steam/apps/2050650/library_600x900.jpg) | `capa-resident-evil-4.jpg` |

**Observações sobre as capas de jogos mobile e de Fortnite/Mario Kart:** para jogos mobile (Brawl Stars, Clash of Clans, Genshin Impact, Minecraft e Free Fire) a "capa" é o ícone oficial do app na loja (imagem quadrada), pois esses jogos não possuem arte de capa vertical. Os ícones refletem a arte vigente nas lojas na data da coleta (o do Free Fire e o do Genshin Impact têm temática de evento/marca da publicadora). O Mario Kart 8 Deluxe usa a imagem horizontal da página oficial da Nintendo e o Fortnite usa arte vertical de uma temporada. Todas são exibidas inteiras, sem corte nem distorção.

**League of Legends** segue com uma ilustração SVG original provisória: não foi encontrada imagem oficial inequívoca do jogo para PC (as páginas oficiais retornaram apenas imagens de notícias, logos da Riot Games ou o ícone de *Wild Rift*, que é outro jogo). Esta é a única capa pendente.

## Como Executar

Use um servidor local (necessário para carregar as legendas `<track>`, que o navegador bloqueia em `file://`):

1. Clone ou baixe este repositório.
2. Na pasta do projeto, execute: `python -m http.server 8000`
3. Acesse `http://localhost:8000` no navegador.

O vídeo de destaque não acompanha o repositório: adicione `assets/videos/destaque.mp4` (e, opcionalmente, `destaque.webm`) para ativar o player. Sem ele, a página mostra um aviso.

## Avaliação em Pares

Esta seção será preenchida conforme as orientações da disciplina, incluindo as avaliações realizadas pelos integrantes do grupo.

# Relatório de Avaliação por Pares das Atividades Práticas

**Disciplina:** Desenvolvimento Front-end para Web
**Projeto avaliado:** projeto-integrador-frontend-henrique-duarte (GAMEVERSE, Catálogo Interativo de Jogos)
**Repositório:** https://github.com/henriquepontesduarte13013-ctrl/projeto-integrador-frontend-henrique-duarte
**Autor do projeto:** Henrique Duarte
**Revisor:** Eduardo França Lins de Albuquerque
**Escopo:** Aulas 1 a 15, conforme o checklist da Seção 6 do Guia do Aluno
**Data da análise:** 23 de novembro de 2026


## 1. Auditoria Lighthouse utilizada como evidência

| Categoria | Pontuação |
|---|---|
| Performance | 97 |
| Accessibility | 100 |
| Best Practices | 100 |
| SEO | 100 |

---

## 2. Resultados por aula

### Aula 1: Git e GitHub

| Critério | Avaliação | Pontos | Evidência |
|---|---|---|---|
| Repositório público e documentado | Atende Plenamente | 2 | O repositório é público. O `README.md` descreve o projeto, as funcionalidades, a estrutura de arquivos, as instruções de execução e a origem de cada imagem. |
| Histórico de commits | Atende Plenamente | 2 | Os commits descrevem a alteração realizada, por exemplo "feat: adiciona interatividade ao GAMEVERSE" e "Implement favorite games functionality with localStorage". Não há mensagens genéricas como "update" ou "teste". |
| Uso de branch e Pull Request | Atende Plenamente | 2 | Foram usadas cinco branches de funcionalidade (`feature/dom-interatividade` e `feature/etapa-1` a `etapa-4`), todas integradas à `main` por Pull Request (#1 a #5). |
| `.gitignore` presente | Atende Plenamente | 2 | O arquivo existe e contém `node_modules/`. |

**Pontos: 8 de 8. Nota: 10,0.**

### Aula 2: Conceitos Fundamentais da Web

| Critério | Avaliação | Pontos | Evidência |
|---|---|---|---|
| HTML mínimo válido | Atende Plenamente | 2 | `index.html` contém `<!DOCTYPE html>`, `<html lang="pt-BR">`, `<head>` e `<body>` corretamente estruturados. |
| Página abre sem erros | Atende Plenamente | 2 | Nenhum erro na execução dos testes. Best Practices 100 no Lighthouse indica ausência de erros registrados no console. Todos os arquivos referenciados existem, exceto os vídeos, que a página não requisita enquanto `data-disponivel="false"`. |
| Meta tags básicas | Atende Plenamente | 2 | `charset` (linha 4) e `viewport` (linha 5) presentes no `<head>`. SEO 100 no Lighthouse. |

**Pontos: 6 de 6. Nota: 10,0.**

### Aula 3: HTML5, Semântica e Formulários

| Critério | Avaliação | Pontos | Evidência |
|---|---|---|---|
| Elementos semânticos | Atende Plenamente | 2 | Uso de `<header>` (linha 68), `<nav>` (69), `<main>` (99), `<section>` (100, 105, 131, 152), `<footer>` (173) e `<article>` (gerado em `catalogo.js`, linha 157). |
| Labels associados aos campos | Atende Plenamente | 2 | O único campo (`#campo-busca`, linha 114) possui `<label for="campo-busca">` (linha 110). |
| Validação nativa usada | Atende Plenamente | 2 | O campo usa `type="search"`, coerente com o dado esperado. Por ser um campo de filtro, a ausência de `required` é adequada. |

**Pontos: 6 de 6. Nota: 10,0.**

### Aula 4: HTML5, Recursos Multimídia

| Critério | Avaliação | Pontos | Evidência |
|---|---|---|---|
| Fallback de formato | Atende Parcialmente | 1 | A lógica para múltiplos formatos está implementada de forma correta: `main.js` (linha 117) cria elementos `<source>` com o tipo adequado para mp4 e webm a partir de `data-mp4` e `data-webm`. A ressalva é que o `index.html` não possui `<source>` estático e a pasta `assets/videos/` contém apenas `.gitkeep`. Sem os arquivos de vídeo, o fallback não pode ser observado em funcionamento. Com os arquivos no repositório, o critério seria plenamente atendido. |
| Atributo `controls` presente | Atende Plenamente | 2 | O `<video>` (linha 137) possui `controls`. Não há `autoplay`. |
| `preload` configurado com critério | Atende Plenamente | 2 | `preload="metadata"` é adequado a um vídeo de destaque que não deve ser baixado integralmente antes da interação. |

**Pontos: 5 de 6. Nota: 8,3.**

### Aula 5: HTML5, Recursos Gráficos (Canvas/SVG)

| Critério | Avaliação | Pontos | Evidência |
|---|---|---|---|
| Escolha da tecnologia justificada | Atende Plenamente | 2 | SVG é usado para ícones, logotipo e favicon (sprite com `<symbol>` e `<use>`). Canvas é usado para o gráfico de barras "Favoritos por categoria", que é redesenhado a cada alteração e a cada redimensionamento (`graficos.js`, linhas 159 e 169 a 172). |
| Elemento renderiza corretamente | Atende Plenamente | 2 | O código de desenho executa sem erros e a auditoria não registra erros de console. O gráfico trata todas as categorias, inclusive as sem favoritos, e se adapta ao tamanho do contêiner. |
| Acessibilidade básica em SVG | Atende Plenamente | 2 | Os ícones decorativos usam `aria-hidden="true"`. O Canvas, que tem função informativa, possui `role="img"`, `aria-labelledby` e legenda textual (`aria-describedby`), conforme a linha 163 do `index.html`. A capa em SVG recebe `alt` descritivo. |

**Pontos: 6 de 6. Nota: 10,0.**

### Aula 6: CSS3, Sintaxe, Seletores e Box Model

| Critério | Avaliação | Pontos | Evidência |
|---|---|---|---|
| Seletores eficientes | Atende Plenamente | 2 | Nenhuma ocorrência de `!important` nos arquivos CSS. Os seletores são curtos e baseados em classes. |
| Box model consistente | Atende Plenamente | 2 | `css/reset.css` (linha 4) aplica `box-sizing: border-box` de forma global. |
| CSS organizado | Atende Plenamente | 2 | Os estilos estão em `css/reset.css` e `css/style.css`. Não há atributo `style=` inline no `index.html`. |

**Pontos: 6 de 6. Nota: 10,0.**

### Aula 7: CSS3, Pseudo-classes, Flexbox e Grid

| Critério | Avaliação | Pontos | Evidência |
|---|---|---|---|
| Layout com Flexbox/Grid | Atende Plenamente | 2 | Há 17 declarações `display: flex` ou `grid` e nenhuma ocorrência de `float`. A grade de cards usa `grid-template-columns: repeat(auto-fill, minmax(...))` (linhas 596 e 601). |
| Eixo principal/cruzado corretos | Atende Plenamente | 2 | O uso de `flex-direction`, `align-items` e `justify-content` é coerente com o layout descrito, sem recurso a posicionamento manual para alinhar elementos. |

**Pontos: 6 de 6. Nota: 10,0.**

### Aula 8: CSS3, Menus e Navegação

| Critério | Avaliação | Pontos | Evidência |
|---|---|---|---|
| Menu funcional e responsivo | Atende Plenamente | 2 | Menu hambúrguer em telas pequenas (`#menu-toggle`) e barra horizontal a partir de 48rem. O estado é controlado por `aria-expanded` (`main.js`, linhas 6 a 11), e o menu fecha com a tecla Esc (linha 67) e ao clicar fora. |
| Estados de interação visíveis | Atende Plenamente | 2 | `.nav-link:hover` (linha 124), `.dropdown__menu a:hover` (linha 181) e `:focus-visible` global (linha 32). |
| Sem sobreposição indevida | Atende Plenamente | 2 | O cabeçalho é `sticky` com `z-index: 100` (linhas 54 a 56) e o dropdown possui `max-height` e `overflow-y: auto`, o que evita corte e sobreposição. Não foi identificado nenhum indício em contrário. |

**Pontos: 6 de 6. Nota: 10,0.**

### Aula 9: CSS3, Botões e Formulários

| Critério | Avaliação | Pontos | Evidência |
|---|---|---|---|
| Foco visível em botões/campos | Atende Plenamente | 2 | `:focus-visible` global com contorno de 2 px (linhas 32 a 35). O campo de busca substitui o `outline` por `border-color` e `box-shadow` visíveis (linhas 357 a 361). |
| Hierarquia visual de ações | Atende Plenamente | 2 | A ação principal, "Favoritar", usa a cor primária na borda e recebe preenchimento e destaque quando ativa (`.btn-fav`, linha 293; `.card.favorito .btn-fav`, linha 311). A ação secundária, "Remover", usa cor de texto atenuada e borda neutra (`.btn-remover`, linha 457). A diferença de destaque entre as duas é perceptível. Esta classificação foi revista em relação à avaliação inicial (Atende Parcialmente), após nova leitura dos estilos. |
| Usabilidade nativa preservada | Atende Plenamente | 2 | Os botões usam `type="button"`, o campo usa `type="search"` e a remoção do `outline` no campo é compensada por indicador alternativo. |

**Pontos: 6 de 6. Nota: 10,0.**

### Aula 10: JavaScript, Fundamentos

| Critério | Avaliação | Pontos | Evidência |
|---|---|---|---|
| Função resolve o problema proposto | Atende Plenamente | 2 | As funções `normalizar` e `jogoCorresponde` (`catalogo.js`) retornaram o resultado esperado nos testes: a busca "ragnarok" localizou "God of War Ragnarök" e "ZELDA" localizou um único jogo. O filtro por categoria "RPG" retornou 3 jogos, conforme os dados. |
| Variáveis com nomes significativos | Atende Plenamente | 2 | Nenhuma ocorrência de `var`. Uso de `let` e `const` com nomes descritivos (`obterFavoritos`, `salvarFavoritos`, `alternarFavorito`). |
| Testado no console | Atende Plenamente | 2 | Nenhum erro nos testes executados e Best Practices 100 no Lighthouse. |

**Pontos: 6 de 6. Nota: 10,0.**

### Aula 11: DOM e Armazenamento Local

PR avaliado: #1, aberto a partir de `feature/dom-interatividade` e integrado à `main`.

| Critério | Avaliação | Pontos | Evidência |
|---|---|---|---|
| Script protegido por `DOMContentLoaded` | Atende Plenamente | 2 | No PR #1, todo o conteúdo de `app.js` está dentro do ouvinte de `DOMContentLoaded` (linha 1), e o `<script>` usa `defer` (`Index.html`, linha 36). Na `main`, os três scripts usam `defer` e a inicialização ocorre em `DOMContentLoaded` (`main.js`, linha 135). |
| Persistência funciona de verdade | Atende Plenamente | 2 | No teste, o jogo favoritado foi salvo na chave `jogosFavoritos` e reaplicado após o recarregamento (classe `favorito` e botão "★ Favoritado"). A chamada `atualizarVisualizacao()` na carga (linha 46) garante a restauração do estado. Desfavoritar atualiza o armazenamento para uma lista vazia. |
| Event delegation em listas | Atende Plenamente | 2 | No PR #1 existe um único `addEventListener('click')`, no elemento pai `#grade-itens` (linha 28), com `evento.target.closest('.btn-fav')`. Na `main`, a grade e a lista de favoritos possuem um ouvinte cada (`catalogo.js`, linhas 311 e 318), sem ouvintes por item. |
| `textContent` para dado do usuário | Atende Plenamente | 2 | Nenhuma ocorrência de `innerHTML`, `outerHTML`, `insertAdjacentHTML` ou `document.write` em qualquer arquivo. Todo texto dinâmico é inserido por `textContent`. |
| PR na branch correta | Atende Plenamente | 2 | O PR #1 foi aberto a partir de `feature/dom-interatividade`. |

**Pontos: 10 de 10. Nota: 10,0.**

### Aula 12: Frameworks, Bootstrap

Não possui nenhum arquivo referente ao bootstrap

**Pontos: 0 de 10. Nota: 0,0.**

### Aula 13: Engenharia de Prompt e IA
 
Evidência de uso de IA: os commits que originaram os PRs #2 a #5 (`feat: estrutura-base do GAMEVERSE`, `feat: adiciona interatividade ao GAMEVERSE`, `feat: adiciona multimidia e expande catalogo para 30 jogos` e `feat: finaliza identidade visual do GAMEVERSE com capas reais`) trazem o trailer `Co-Authored-By: Claude Sonnet 5.5`. Isso indica que boa parte do código atual (estrutura, interatividade, multimídia e acabamento visual) foi produzida com apoio de IA. Esta classificação foi revista em relação à versão anterior deste relatório, que não havia considerado o corpo das mensagens de commit.
 
| Critério | Avaliação | Pontos | Evidência |
|---|---|---|---|
| Dois prompts documentados | Não Atende | 0 | O README não documenta o prompt vago inicial nem o prompt reforçado, nem a comparação entre os resultados. As descrições dos PRs não puderam ser lidas (seção 1.4). Se estiverem nos PRs #2 a #5, o critério deve ser reavaliado. |
| Sem incompatibilidade de stack | Atende Plenamente | 2 | O código produzido com apoio de IA está plenamente adaptado à stack real do projeto: HTML5, CSS3 e JavaScript puro (Vanilla JS), sem React, Vue ou qualquer biblioteca estranha. Não há dependências externas, e as imagens são carregadas localmente. |
| Navegável por teclado | Atende Plenamente | 2 | Os componentes interativos (botões de favoritar e remover, chips de categoria, menu e dropdown) usam elementos nativos `<button>` e `<a>`, acionáveis por Tab, Enter e Espaço. Há tratamento da tecla Esc e devolução de foco (`main.js`, linhas 48 a 80) e foco visível global (`style.css`, linha 32). Accessibility 100 no Lighthouse. |
| Nada quebrado | Atende Plenamente | 2 | As funcionalidades das aulas anteriores (persistência em `localStorage`, event delegation, filtros e favoritos) foram preservadas e ampliadas na `main`. Nos testes, favoritar, desfavoritar e recarregar mantiveram o comportamento esperado. |
| PR na branch correta | Não Atende | 0 | A branch `feature/componente-ia` não existe. Os PRs com participação de IA foram abertos a partir de `feature/etapa-1` a `etapa-4`. |
 
**Pontos: 6 de 10. Nota: 6,0.**

### Aula 14: Acessibilidade e Boas Práticas

| Critério | Avaliação | Pontos | Evidência |
|---|---|---|---|
| Auditoria documentada | Atende Parcialmente | 1 | A auditoria Lighthouse informada apresenta Accessibility 100 (seção 1.2), o que comprova o resultado final. Faltam a pontuação anterior às correções, necessária para a comparação "antes e depois", e o registro na descrição do PR. |
| Pelo menos 4 correções reais | Atende Plenamente | 2 | O código contém cinco soluções de acessibilidade acompanhadas de comentário: fechamento do menu e do dropdown com Esc, com devolução do foco ao botão de origem (`main.js`, linha 65); retorno do foco após a escolha de uma categoria (linha 55); fechamento do dropdown quando o foco sai dele por Tab (linha 80); escolha do botão que recebe o foco de volta conforme o menu visível (linha 48); e alternativa textual para o gráfico em Canvas (`graficos.js`, linha 136). Há ainda soluções sem comentário: `aria-label` dinâmico nos botões de remoção (`catalogo.js`, linha 270), `aria-pressed` nos botões de favorito e `aria-expanded` no botão de menu. Os comentários descrevem a solução, e o problema original é subentendido; ver recomendação 4.2.3. |
| Sem elemento clicável não-semântico | Atende Plenamente | 2 | Nenhuma ocorrência de `onclick`. Todos os elementos interativos são `<button>` ou `<a>`. |
| Foco visível em tudo | Atende Plenamente | 2 | `:focus-visible` global (`style.css`, linha 32) cobre os elementos interativos, e o campo de busca tem indicador próprio (linhas 357 a 361). |
| PR na branch correta | Não Atende | 0 | A branch `feature/acessibilidade` não existe no repositório. |

**Pontos: 7 de 10. Nota: 7,0.**

### Aula 15: DNS, Domínios, SSL e Deploy

| Critério | Avaliação | Pontos | Evidência |
|---|---|---|---|
| Site publicado e sem 404 | Não Atende | 0 | Não há URL de publicação no repositório, e a auditoria informada não identifica o endereço em que foi executada. |
| Sem caminho absoluto quebrado | Atende Plenamente | 2 | Nenhum `href` ou `src` começa com `/`. Todos os caminhos são relativos. |
| Funcionalidades testadas no ar | Não Atende | 0 | Sem site publicado identificado, não há evidência de teste. |
| Link documentado no README | Não Atende | 0 | O README não contém o link público do site. |
| HTTPS confirmado | Não Atende | 0 | Não verificável sem a URL. |

**Pontos: 2 de 10. Nota: 2,0.**

---

## 3. Comentários construtivos

### 3.1 Pontos fortes

- **Qualidade medida.** Os resultados da auditoria Lighthouse (Performance 97, Accessibility 100, Best Practices 100, SEO 100) confirmam a qualidade técnica do projeto.
- **Documentação.** O README é detalhado e inclui a estrutura de pastas, as instruções de execução e uma tabela com a origem de cada imagem, acompanhada de aviso sobre direitos autorais.
- **Organização do código.** O JavaScript está dividido por responsabilidade (`catalogo.js`, `graficos.js`, `main.js`), com funções curtas e nomes que explicam sua finalidade. A comunicação entre os módulos por meio de `CustomEvent` (`favoritos:alterados`) é uma solução adequada.

### 3.2 Pontos de melhoria

1. **Vídeo de destaque (Aula 4).** Incluir os arquivos `destaque.mp4` e `destaque.webm` em `assets/videos/`, ou declarar elementos `<source>` diretamente no HTML, para que o fallback de formato possa ser verificado por qualquer revisor.
2. **Publicação (Aula 15).** Publicar o projeto no GitHub Pages e registrar o link no README.

---

## 4. Considerações finais

O projeto apresenta desempenho consistente e sólido nas Aulas 1 a 11, com código legível, boa documentação e resultados excelentes na auditoria Lighthouse. As notas reduzidas concentram-se nas Aulas 12 a 15, em que não foram encontradas as branches e as evidências exigidas pelo checklist.
=======
**Avaliações pendentes:** aguardando realização e preenchimento.