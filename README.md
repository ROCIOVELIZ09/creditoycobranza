# Crédito y Cobranza: módulo de análisis de cartera por cobrar

Página HTML autocontenida (`index.html`) para analizar la cartera por cobrar en USD. Reemplaza el cruce manual de archivos de Excel con BUSCARV.

Los archivos se procesan solo en el navegador. No se suben a ningún servidor.

## Cómo usarlo
1. Abra `index.html` en Chrome, Edge o Safari, con doble clic o desde GitHub Pages.
2. En **Carga y configuración**, arrastre los archivos:
   - **Cartera** (obligatorio).
   - **Maestro de clientes**, **vendedores**, **pagos/cobros** y **ventas/facturación** (opcionales).
3. Revise cómo se interpretó cada columna y corrija lo que haga falta con las listas desplegables.
4. Para ver el funcionamiento con datos ficticios, pulse **Probar con datos de ejemplo**.

La primera vez se necesita internet para descargar SheetJS 0.18.5 desde cdnjs, que lee y escribe Excel. Los archivos CSV funcionan sin conexión.

## Qué incluye
- **Antigüedad de la cartera** por tramos, con detección de partidas por conciliar (posibles retenciones) y saldos a favor.
- **Indicadores**: morosidad, mora ponderada, DSO, días promedio de pago, provisión estimada (NIIF 9), concentración y cobros del mes.
- **Tendencias y proyección**: historial de cortes, ventas y cobros mensuales y anuales, y proyección de cobros a 13 semanas y 6 meses.
- **Clientes**: score interno A/B/C/D, ficha por cliente y bitácora de gestiones con promesas de pago.
- **Alertas** por prioridad (alta, media, baja), con mensaje de cobranza para copiar o enviar por WhatsApp o correo.
- **Exportación**: reporte Excel completo y respaldo en `.json`.

Los datos se guardan en el `localStorage` del navegador.
