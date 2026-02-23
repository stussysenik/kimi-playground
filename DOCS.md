# Technical Documentation

## Architecture

The project uses a standard Vite + React SPA architecture:

```
Browser → Vite Dev Server (HMR) → React 19 (createRoot) → Component Tree
```

**Build pipeline:** TypeScript (`tsc -b`) → Vite bundler → optimized static assets

## Component Structure

### App.tsx
Root component using React `useState` hook. Renders the Vite and React logos with hover animations, an interactive counter button, and instructional text. Serves as the starting point for wireframe development.

### main.tsx
Entry point that mounts the App component into `#root` using React 19's `createRoot` API, wrapped in `StrictMode` for development warnings.

## TypeScript Configuration

Three-file setup:
- **tsconfig.json** — Base references, includes app + node configs
- **tsconfig.app.json** — App code: ES2022 target, bundler module resolution, strict mode, JSX automatic runtime
- **tsconfig.node.json** — Tooling code: ES2023 target, for vite.config.ts and build scripts

## Development Workflow

1. `npm run dev` — Start Vite dev server with HMR on port 5173
2. Edit `.tsx` files — Changes reflect instantly via React Fast Refresh
3. `npm run lint` — Check code quality with ESLint
4. `npm run build` — Type-check then bundle for production
5. `npm run preview` — Serve the production build locally

## Styling

- **index.css** — Global resets, font stack, dark/light theme via `prefers-color-scheme`
- **App.css** — Component-scoped styles with logo animations, card layout, button states
- Color scheme: Dark by default, respects system preference
