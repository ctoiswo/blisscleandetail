# BlissClean – Correr en Local

Proyecto HTML estático puro. Sin build, sin dependencias.

## Opción 1: VS Code Live Server (recomendado)

1. Instalar extensión **Live Server** en VS Code
2. Click derecho en `index.html` → **Open with Live Server**
3. Abre `http://localhost:5500`

## Opción 2: Python (sin instalar nada extra)

```bash
# Python 3
python3 -m http.server 8080

# Python 2
python -m SimpleHTTPServer 8080
```

Abre `http://localhost:8080`

## Opción 3: Node.js (`serve`)

```bash
npx serve .
```

Abre la URL que muestra en terminal (normalmente `http://localhost:3000`).

## Opción 4: Vercel CLI (simula producción exacta)

```bash
npm i -g vercel
vercel dev
```

Abre `http://localhost:3000`. Aplica headers y rewrites de `vercel.json`.

---

## Rutas disponibles

| URL | Archivo |
|-----|---------|
| `/` | `index.html` |
| `/bookdetail` | `index.html` (rewrite) |
| `/privacy-policy` | `privacy-policy.html` |
| `/terms` | `terms.html` |

> Los rewrites de `vercel.json` solo funcionan con **Vercel CLI**. Con Python/Live Server, accede directo al `.html`.

## Producción

Deploy en Vercel. Push a `main` = deploy automático.
