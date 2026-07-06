## Development

Astro single-page site. Tailwind CSS v4 via `@tailwindcss/vite`. No external CDN.

To start the dev server:

```bash
pnpm install      # only the first time
pnpm dev          # serves the project at http://localhost:4321/
```

The server runs in the foreground. To stop it, press `Ctrl+C`.

## Project structure

```
.
├── index.html         # not committed — built output goes to dist/
├── astro.config.mjs   # Tailwind v4 Vite plugin
├── package.json       # astro + tailwindcss
├── tsconfig.json
├── src/
│   ├── layouts/
│   │   └── Base.astro      # html shell, head, fonts, scripts
│   ├── components/
│   │   ├── Nav.astro
│   │   ├── Hero.astro
│   │   ├── Marquee.astro
│   │   ├── Services.astro
│   │   ├── ServiceCard.astro
│   │   ├── Proceso.astro
│   │   ├── Resultados.astro
│   │   ├── Testimonio.astro
│   │   ├── Nosotros.astro
│   │   ├── Contacto.astro
│   │   └── Footer.astro
│   ├── pages/
│   │   └── index.astro     # composes all components
│   └── styles/
│       └── global.css      # Tailwind import, @theme tokens, utility classes
├── CONTENT.md        # inventory of all text content (ES/EN reference)
├── AGENTS.md         # this file
├── CLAUDE.md         # symlink to AGENTS.md
└── README.md
```

## Stack

- Astro 7
- Tailwind CSS v4 (build step, no CDN)
- Google Fonts (Inter + Space Grotesk)
- Vanilla JS in Base.astro (form submit + scroll-spy)
- No frameworks, no i18n, no CMS, no API

## Editing content

All content lives directly inside the component files. There is no i18n, no CMS, no content collections.

If you ever need translations or a content layer, introduce them at that point.