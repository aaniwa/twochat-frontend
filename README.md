# Frontend (Cloudflare Pages)

This folder is ready to be used as a standalone frontend repository.

## Local development

```bash
npm install
npm run dev
```

By default, local dev uses Vite proxy for `/api` and `/socket.io`.

## Environment variables

Copy `.env.example` to `.env` (or set variables in Cloudflare Pages):

- `VITE_API_BASE_URL`: backend base URL (no trailing slash), example `https://api.example.com`
- `VITE_SOCKET_URL`: optional socket base URL; if omitted, frontend reuses `VITE_API_BASE_URL`
- `VITE_DEV_API_PROXY_TARGET`: local proxy target for `npm run dev`

## Build

```bash
npm run build
```

Output goes to `dist/`.

## Cloudflare Pages settings

- Build command: `npm run build`
- Build output directory: `dist`

`public/_redirects` is included for SPA route fallback.
# twochat-frontend
