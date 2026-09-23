# RL Map Placer

Herramienta de posicionamiento manual para los meshes extraídos de
`Complexityv106.udk`. Todo el 3D corre en el navegador (Three.js vía CDN);
no hay backend ni build step.

## Deploy en Vercel

1. Subí esta carpeta a un repo de GitHub.
2. En Vercel: "New Project" → importá el repo.
3. Framework Preset: **Other** (sitio estático). No hace falta build command
   ni output directory — Vercel sirve `index.html` directo.
4. Deploy.

## Deploy local rápido (sin Vercel)

Cualquier servidor estático sirve, por ejemplo:

```bash
python3 -m http.server 8000
```

y abrís `http://localhost:8000` en el celular (misma red Wi-Fi) o en la
compu.

## Uso

Ver instrucciones dentro de la propia página. Al terminar de ubicar los
meshes, el botón "JSON" exporta las transforms (posición/rotación/escala)
para pegarlas de vuelta en la conversación con Claude, que arma el `.glb`
final con esas coordenadas.

Los datos de geometría de los 41 meshes están embebidos directamente en
`index.html` (base64), así que el sitio es 100% estático y autocontenido —
no necesita ningún otro archivo ni API.
