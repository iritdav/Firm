# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Layout

The git root contains a single app, `FirmApp/` (Vue + Vite, freshly scaffolded from the `create-vue` template). Run all npm commands from `FirmApp/`.

## Commands

```sh
npm install        # requires Node ^22.18.0 or >=24.12.0
npm run dev        # Vite dev server with HMR (includes vite-plugin-vue-devtools)
npm run build      # production build to dist/
npm run preview    # serve the production build
npm run format     # prettier --write on src/
```

There is no test runner or linter configured.

## Notes

- Uses the **Vue release-candidate** (`"vue": "rc"`); `package.json` `overrides` pins all `@vue/*` packages (including `compiler-vapor` and `runtime-vapor`) to `rc` too. Keep them in sync when changing Vue dependencies.
- Entry point: `src/main.js` mounts `src/App.vue` on `#app` and imports `src/assets/main.css`. `src/components/` is still the template's welcome/demo content (HelloWorld, TheWelcome, icons).
- `@` aliases `src/` (configured in both `vite.config.js` and `jsconfig.json`).
- Prettier style: no semicolons, single quotes, 100-column width.
