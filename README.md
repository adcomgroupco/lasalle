# La Salle

Sitio de consulta de reportes de campañas de La Salle Pereira (Meta y Google Ads).

## Contenido

- `index.html`: página principal.
- `reporte-semanal.html`: reporte semanal de Meta y Google con filtro de fechas, frente al presupuesto del flow, con ritmo de inversión del mes.
- `data/lasalle_daily.js`: datos diarios por campaña que lee el reporte semanal.
- `assets/`: estilos del sitio.

## Uso local

Abre `index.html` en un navegador.

## Actualizar el reporte semanal

Los datos se generan desde el repositorio Meta-Ads-CLI:

```
.venv/bin/python scripts/clients/lasalle/build_lasalle_weekly.py
```

Los presupuestos por campaña y mes están en `FLOW`, dentro de `reporte-semanal.html`. La sección "Lectura" es texto fijo: se reescribe en cada entrega.
