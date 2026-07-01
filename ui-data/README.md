# Dashboard — Salud Mental en Adolescentes

Dashboard web interactivo que presenta de forma visual el paper científico del
proyecto de **Manejo de Datos para la IA** (Universidad Galileo). Recorre todo el
análisis: EDA, comparativa de modelos, mejoras metodológicas (SMOTE, RandomizedSearch,
detección de anomalías, RFE), reevaluación del target y el modelo final de predicción
de depresión.

Construido con [Astro](https://astro.build) y [Chart.js](https://www.chartjs.org).

## Requisitos

- Node.js 18+
- `pnpm` (recomendado) o `npm`

## Cómo levantarlo

```bash
pnpm install      # o: npm install
pnpm dev          # o: npm run dev
```

Abre la URL que imprime la terminal (por defecto `http://localhost:4321`).

## Comandos

| Comando | Acción |
|---|---|
| `pnpm install` | Instala dependencias |
| `pnpm dev` | Servidor de desarrollo en `localhost:4321` |
| `pnpm build` | Genera el sitio estático en `dist/` |
| `pnpm preview` | Sirve el build de producción localmente |

## Estructura

```
src/
├── components/        # Secciones del dashboard (.astro)
├── data/
│   └── results.json   # Todos los datos y métricas que renderiza la UI
├── layouts/
└── pages/
    └── index.astro    # Página única que compone las secciones
public/charts/         # Gráficas exportadas del notebook
```

> Para cambiar números o textos del dashboard, edita `src/data/results.json`:
> los componentes leen sus datos de ahí.
