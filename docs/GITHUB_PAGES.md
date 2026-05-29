# GitHub Pages (demo en tu fork)

1. En GitHub: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
2. Push a `main` (el workflow `.github/workflows/deploy.yml` buildea y publica `dist/`).
3. La demo queda en: https://igor-streiff.github.io/VoxelParty/

## Signaling para visitantes remotos

La app usa WebRTC P2P; hace falta un servidor de **signaling** (WebSocket) para que los navegadores se encuentren.

- Hoy: `wss://voxelparty-signaling.onrender.com` (infra del equipo del curso; plan free puede dormir).
- Para portfolio estable: desplegar la carpeta [`signaling/`](../signaling/) en [Render](https://render.com) y actualizar `SIGNALING_SERVERS` en `src/sync.js`.

Prueba local con dos pestanas en la misma maquina suele funcionar aun si el signaling publico esta lento.
