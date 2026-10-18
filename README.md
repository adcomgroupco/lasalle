# La Salle

Sitio de consulta de reportes, planeación, creatividad e informes de las campañas de La Salle Pereira Bilingual School en Meta y Google Ads.

## Contenido

- `index.html`: página principal, con los documentos por sección.
- `reporte-semanal.html`: reporte semanal de Meta y Google con filtro de fechas, frente al presupuesto del flow, con ritmo de inversión del mes.
- `flow-general.html`: flow global 2026, distribución mensual y plan de septiembre–octubre.
- `segmentacion-meta.html`: segmentación de Meta Ads, versión 4.
- `palabras-clave-google-ads.html`: juego de palabras clave de Google Ads, versión 2.
- `brief-audiovisual.html`: brief de los ocho reels de 2026.
- `informe-abril-mayo-2026.html` y `analisis-palabras-clave-search.html`: informes.
- `informes/`: reportes de implementación en PDF, con el prefijo `AAAA-MM`.
- `archivos/`: originales descargables (xlsx, docx, md) de los documentos de planeación y creatividad.
- `data/lasalle_daily.js`: datos diarios por campaña que lee el reporte semanal.
- `assets/css/`: `adcom.css` (base) y `documento.css` (páginas de documento).

## Uso local

Abre `index.html` en un navegador.

## Convención de nombres

Los archivos de contenido usan `kebab-case`. Los documentos estándar de GitHub conservan sus nombres convencionales, por ejemplo `README.md`.

## Actualizar el reporte semanal

Los datos se generan desde el repositorio Meta-Ads-CLI:

```
.venv/bin/python scripts/clients/lasalle/build_lasalle_weekly.py
```

Los presupuestos por campaña y mes están en `FLOW`, dentro de `reporte-semanal.html`. La sección "Lectura" es texto fijo: se reescribe en cada entrega.

Las páginas de flow, segmentación, palabras clave y brief son copias convertidas de los archivos en `archivos/`. Si cambia el original, hay que volver a generar la página.
