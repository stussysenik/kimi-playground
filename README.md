# kimi-playground

A wireframe site built with React 19, Vite 7, and TypeScript 5.9. Serves as a playground for prototyping UI layouts and interactive components.

## Tech Stack

- **React** 19.2.0 — UI framework
- **Vite** 7.3.1 — Build tool with HMR
- **TypeScript** 5.9.3 — Strict type checking
- **ESLint** 9.39.1 — Linting with TypeScript + React hooks rules

## Quick Start

```bash
cd wireframe-site
npm install
npm run dev
```

Open `http://localhost:5173` in your browser.

## Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start dev server with HMR |
| `npm run build` | Type-check and build for production |
| `npm run lint` | Run ESLint |
| `npm run preview` | Preview production build |

## Project Structure

```
kimi-playground/
├── wireframe-site/         # Main React application
│   ├── src/
│   │   ├── App.tsx         # Root component (counter demo + layout)
│   │   ├── App.css         # Component styles (dark theme, hover effects)
│   │   ├── main.tsx        # Entry point (React 19 createRoot)
│   │   └── index.css       # Global styles (dark/light theme support)
│   ├── public/             # Static assets
│   ├── package.json
│   ├── vite.config.ts
│   ├── tsconfig.json       # Base TypeScript config
│   ├── tsconfig.app.json   # App-specific TS config (ES2022, strict)
│   ├── tsconfig.node.json  # Node tooling TS config (ES2023)
│   └── eslint.config.js    # Flat ESLint config
└── nvim-portable/          # Portable Neovim configuration
```

## Features

- Dark/light theme support via CSS media queries
- Hot Module Replacement for instant feedback
- Strict TypeScript with no unused locals/parameters
- ESM module system throughout
