# Salud Mental en Adolescentes y Uso de Redes Sociales

Proyecto de **Manejo de Datos para la IA** — Postgrado de Inteligencia Artificial,
Universidad Galileo. Clasificación supervisada sobre el dataset *Teen Mental Health
& Social Media* (Kaggle), con un enfoque **metodológico**: cómo el análisis EDA
diagnostica que una *accuracy* alta puede ser un espejismo y guía hacia el modelo
correcto.

## Contenido del repositorio

| Archivo | Descripción |
|---|---|
| `salud_mental_adolescentes.ipynb` | Notebook con todo el análisis y los modelos (EDA → mejoras → modelo final) |
| `paper_manejo-datos-IA.pdf` | **Paper científico (PDF de entrega)** |
| `Teen_Mental_Health_Dataset.csv` | Dataset (1.200 registros, 13 columnas) |
| `ui-data/` | Dashboard web interactivo (Astro) que presenta el paper de forma visual |
| `requirements.txt` | Dependencias de Python del notebook |
| `grafica_*.png` | Gráficas generadas por el notebook |

## Cómo levantar la UI (dashboard)

El dashboard está construido con [Astro](https://astro.build) y Chart.js.

**Requisitos:** Node.js 18+ y `pnpm` (o `npm`).

```bash
cd ui-data
pnpm install          # o: npm install
pnpm dev              # o: npm run dev
```

Abre la URL que imprime la terminal (por defecto `http://localhost:4321`).

**Otros comandos:**

```bash
pnpm build            # genera el sitio estático en ui-data/dist/
pnpm preview          # sirve el build de producción localmente
```

Para publicar (GitHub Pages, Netlify, Vercel): sube el contenido de `ui-data/dist/`.

## Cómo correr el notebook

```bash
python -m venv venv && source venv/bin/activate
pip install -r requirements.txt
jupyter notebook salud_mental_adolescentes.ipynb
```

> El notebook descarga el dataset desde Kaggle usando credenciales en un archivo
> `.env` (`KAGGLE_USERNAME`, `KAGGLE_KEY`). El CSV ya está incluido en el repo, así
> que puedes saltarte esa celda y ejecutar **Run All** desde la sección 3.
> Las secciones 11–15 reutilizan variables de secciones previas: ejecútalo en orden.


---