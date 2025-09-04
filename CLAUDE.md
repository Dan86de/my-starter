# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a TanStack Start (React) application with TypeScript, configured with Vite as the build tool and Biome for linting/formatting. The project uses TanStack Router for client-side routing and Tailwind CSS for styling.

## Common Commands

- `pnpm dev` - Start development server (runs on port 3000)
- `pnpm build` - Build for production
- `pnpm lint` - Lint code with Biome (auto-fixes issues)
- `pnpm format` - Format code with Biome

## Architecture

### Routing
The application uses TanStack Router with file-based routing:
- Routes are defined in `src/routes/` directory
- `__root.tsx` contains the root layout with HTML document structure
- `routeTree.gen.ts` is auto-generated (excluded from Biome linting)
- Router configuration is in `src/router.tsx`

### Styling
- Global styles in `src/styles/global.css`
- Tailwind CSS configured via Vite plugin
- Uses CSS imports with `?url` for stylesheet loading

### TypeScript Configuration
- Strict TypeScript configuration with path aliases (`~/*` maps to `./src/*`)
- ES modules with bundler resolution
- Target ES2022 with DOM libraries

### Code Quality
- Biome handles both linting and formatting
- Configured for tab indentation and double quotes
- Auto-sorts Tailwind classes
- Removes unused imports automatically
- Excludes generated files from linting
