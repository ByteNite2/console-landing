# console-landing

Static clone of the ByteNite auth UI surface, served at **console.bytenite.com** via GitHub Pages.

## What this is

A frozen snapshot of the `new-auth-ui` React SPA (Vite build) extracted from
`europe-west3-docker.pkg.dev/transcoding-testing/bytenite-dev/bytenite-new-auth-ui:69790900`
on 2026-04-24, after GCP wind-down tore down the live cluster.

**The UI renders but does not function.** All API calls go to `api.bytenite.com`,
`auth.bytenite.com`, etc., which no longer resolve. Forms will show network errors
on submit. This exists only so `console.bytenite.com` doesn't return 404.

## Source of truth

Built from [ByteNite2/bytenite-auth-ui-v2](https://github.com/ByteNite2/bytenite-auth-ui-v2)
at revision `697909000ee30340f93f621bee7f26af93e33b67` (2025-09-15).

## Hosting

- GitHub Pages from `main` branch root.
- Custom domain: `console.bytenite.com` (CNAME file).
- Cloudflare A records → GitHub Pages IPs:
  - 185.199.108.153
  - 185.199.109.153
  - 185.199.110.153
  - 185.199.111.153
  - (AAAA for IPv6: `2606:50c0:8000::153`, `::8001::153`, `::8002::153`, `::8003::153`)
