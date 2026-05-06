# Quadro Operacional — Grupo Cantucci

## Stack
- HTML/CSS/JS puro — sem build, sem framework, sem Node
- Arquivo único: `index.html` (~81 KB, tudo inline)
- Libs via CDN: `chart.js@4.4.0`, `html2canvas@1.4.1`
- Deploy automático no GitHub Pages ao fazer push na branch `main`

## Como rodar localmente
Abra `index.html` direto no navegador — não precisa de servidor.
Para evitar problemas com CORS em futuras evoluções, use Live Server (VS Code) ou:
```
npx serve .
```

## Estrutura
```
quadro-operacional/
├── index.html          # app inteiro (HTML + CSS + JS)
├── .github/
│   └── workflows/
│       └── deploy.yml  # GitHub Actions → GitHub Pages
└── .gitkeep
```

## Convenções
- Todo o CSS fica no `<style>` no `<head>`, antes do JS
- Todo o JS fica em `<script>` no final do `<body>`
- Telas são `<div class="screen">`, ativadas com classe `active`
- Paleta: preto `#1a1a1a`, verde `#1D9E75`, azul `#185fa5`
- Mobile-first: max-width 440px centralizado

## Deploy
Push na `main` → GitHub Actions publica automaticamente no GitHub Pages.
