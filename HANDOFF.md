# HANDOFF — reportes-play (Reportes Play)

*Creado: 11/10/2026.*

## Qué es
Botón ▶ en los reportes que reproduce una explicación en audio de lo que pasó en el mes. Primero como función del Hub para los clientes de COSMART (versión con branding de viajes); texto neutro para otras agencias. Preview aprobado en artifact: https://claude.ai/artifact/17Jo9Q8CUuqcmYM5GEL9zS (11/10).

## Estado
Repo recién creado, vacío de código. Decisiones tomadas en la sesión "Aplicaciones sin hacer para vender" (11/10):
- Texto de COSMART aprobado por Vaneh (tono de viaje: tramo del viaje, compañeros de ruta, destino). Texto neutro para otras agencias también aprobado.
- Audio: voz del navegador (SpeechSynthesis, es-AR) por ser gratis. Vaneh todavía tiene que probar cómo suena; si es muy robótica, evaluar alternativa GRATUITA y consultarle antes.
- El texto lo genera la IA con datos reales del reporte y Vaneh lo revisa antes de publicar (la IA puede inventar causas).
- Es función del Hub, no app aparte; el repo guarda el componente y el preview.

## Pendiente real
1. Que Vaneh pruebe el audio del preview y diga cómo suena.
2. Leer HANDOFF.md de hub y cosmart-workers y ver cómo están hechos hoy los reportes.
3. Integrar el botón Play al Hub (verificar mobile y que todos los botones funcionen) y subir.

## Reglas duras
- Vaneh se comunica **solo en español** (rioplatense) — nunca respondas en inglés.
- **Nunca hagas cambios no pedidos.** Si algo parece mejorable, preguntá antes.
- **Solo servicios GRATUITOS.** Nada con costo fijo para COSMART (decisión de Vaneh, 11/10). Antes de usar cualquier servicio externo, verificar que sea gratis y avisar si tiene un límite que pueda empezar a cobrar. Sin tarjetas ni planes pagos hasta que haya ingresos y ella lo autorice.
- **Cada app es independiente**: propia landing, propio login, propios usuarios y contraseñas. Quien compra una NO accede al Hub ni a las otras apps.
- **Sin WhatsApp** por ahora (decisión de Vaneh): los avisos van por mail.
- **Texto primero**: todo texto que haya que escribir (mails, copys, explicaciones) se muestra en el chat y se espera aprobación antes de seguir.
- **Landings / páginas nuevas**: primero preview en artifact para que Vaneh corrija ahí mismo. Responsive mobile primero. Texto claro sobre fondos oscuros. Revisar que todos los botones funcionen.
- **Branding COSMART** (para el uso interno y los clientes de COSMART): brújula/viajeros/destinos; Playfair Display + DM Sans; colores `#0D2B6B` `#1A4DAA` `#3A8FC7` `#E02020` `#F2EDE6`. Ver `cosmart-workers/clientes/cosmart/AI_OPERATING_SYSTEM.md`. Para el resto de los clientes de las apps, textos neutros.
- **Cron triggers de Cloudflare: la cuenta está al tope (5/5, Workers Free).** No agregar crons nuevos; reusar uno existente de `cosmart-workers` o consultar a Vaneh. Deploy de workers siempre MANUAL y avisando antes.
- **Rendimiento (que no se rompa al crecer)**: datos en filas chicas e indexadas (D1), nunca bloques JSON gigantes; listas paginadas; carga por partes; envíos de mail en cola con tope diario; topes de clientes por plan; prueba de carga antes de lanzar; medir velocidad antes de sumar funciones.
- **Precios de lanzamiento**: Inicial USD 3/mes (hasta 20 clientes) · Plus USD 5/mes (hasta 50) · Pro USD 8/mes (hasta 150). Anual: pagás 10 meses, usás 12 (USD 30 / 50 / 80). Los 2 meses gratis aplican SOLO al plan anual pagado por adelantado; NO hay meses gratis al inicio. Prueba gratis solo para clientes actuales de COSMART.
