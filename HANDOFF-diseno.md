# HANDOFF — Apps para emprendedores (diseño y estado)
*Actualizado: 13/10/2026 · Pide: Vaneh · Idioma: español rioplatense*

## DECISIONES (13/10) — mandan sobre todo lo demás
- **Marca paraguas: "Al Día"**, con 3 apps: **Al Día Cobros**, **Al Día Voz** y **Al Día IA** (confirmado por Vaneh el 13/10; hubo una confusión pasajera donde la descartó por error). Alternativas que propuso Claude Design y NO se eligieron: Dale, Tranqui, Cuentas Claras, Puntual.
- **Las apps viven dentro de `apps.vamatienda.com.ar`** (dominio de VAMA), pero NO llevan la marca VAMA: la identidad es Al Día. Pendiente de definir: rutas o subdominios de cada app.
- Identidad visual aprobada: dirección 1a "Terracota" (ver `referencia-diseno/Branding_Apps.dc.html`). Gabarito + Figtree, terracota #B4452A, mostaza #E2A33A.
- Pendiente de Vaneh antes de publicar: registro de marca de "Al Día" en AR, CL y UY (Claude Design no lo verificó).

## Contexto
Vaneh tiene una agencia de marketing (COSMART) y lanza 3 apps baratas e independientes para emprendedores y pymes de Latinoamérica. NADA de COSMART en estas apps: ni nombre, ni logo, ni azul marino (#0D2B6B y familia), ni brújula/viajes.

## Las 3 apps (cada una con su propia landing, login y usuarios)
1. **Cobros** (repo `app-cobro`, la primera): recordatorios automáticos de pago por MAIL a los clientes de un emprendedor, ficha de cada cliente (nombre, apellido, mail, teléfono, cumpleaños, plan, fecha de pago, tratamientos, consultas) y mail de cumpleaños.
2. **Voz** (repo `reportes-play`): botón ▶ que lee en voz alta una explicación del reporte/dashboard. Ya programado en el Hub (rama `claude/play-reportes`, sin mergear).
3. **IA** (repo `ia-busquedas`, la última): monitor de si las IA nombran a una marca.

## Precios de lanzamiento
Inicial USD 3/mes (hasta 20 clientes) · Plus USD 5/mes (hasta 50) · Pro USD 8/mes (hasta 150). Anual: pagás 10 meses y usás 12 (USD 30 / 50 / 80). Los 2 meses gratis aplican SOLO al anual pagado por adelantado; no hay meses gratis de entrada. Prueba gratis solo para clientes actuales de COSMART.

## Reglas
- Todo con herramientas GRATUITAS. Sin WhatsApp (avisos por mail).
- Mobile primero, sin scroll horizontal. Texto sobre fondo oscuro siempre blanco.
- Antes de commitear cualquier página nueva: preview en artifact para que Vaneh corrija comentando.
- No inventar testimonios, cifras ni resultados en las landings.
- La explicación del Play se arma con plantillas y los datos reales del panel (sin IA ni costo) y lleva aviso de "generado automáticamente, puede cometer errores". Vaneh NO revisa cada texto.

## Estado (13/10)
- Preview de la tarjeta ▶ con la estética de Claude Design (con el chip "Al Día Voz", correcto): https://claude.ai/artifact/Qz2Xi1nEYfc7ThTwdmQdCB
- La tarjeta nueva está en el código del Hub (rama `claude/play-reportes`), SIN mergear a main.
- Falta: definir rutas bajo `apps.vamatienda.com.ar`, landing de Cobros (preview), login, pantalla Clientes y ficha, mails de recordatorio y cumpleaños.
- Investigación: hay competidores en recordatorios de cobro (Wati, Leadsales, YoFacturo) y en monitor de marca en IA (Ahrefs Brand Radar USD 50-699/mes). El hueco es precio bajo, simpleza y español local.
