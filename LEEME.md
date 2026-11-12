# Marley Coffee · Landing y Portal B2B (v5)

## Archivos del sitio (subir juntos a la misma carpeta del servidor)
- `index.html`: la página completa (HTML, CSS, JS, logo e imágenes del hero ya incluidas).
- `manifest.webmanifest` y `sw.js`: permiten anclar el portal al celular (PWA). Requieren HTTPS.
- `icon-192.png` e `icon-512.png`: íconos de la app.

## Carpetas de apoyo (no es necesario subirlas)
- `imagenes/`: fotos del hero por separado (escritorio y celular), en WebP.
- `capturas/`: capturas de cada flujo de la v4. `m_` = celular, `d_` = escritorio.
- `.claude/`: servidor local y marco para capturas (solo para desarrollo, no subir).

## Novedades de la v5 (rediseño, mobile first, misma paleta)
**Landing**
- Las vistas del prototipo (cliente, marketing y administrador) pasan a un botón discreto «Vistas del prototipo», abajo a la izquierda. La foto de máquinas queda más arriba.
- Primera pantalla con «Cotizar gratis» y tres sellos: factura a tu RUT, despacho en 48 h en la RM y respuesta en 24 h hábiles (plazo de respuesta a cotizaciones del informe, sección 4.1).
- Nuevo orden: beneficios → máquinas → productos → franja WhatsApp → cotización → cómo empiezas → preguntas frecuentes, con fondos alternados (crema, blanco, negro, amarillo suave).
- Máquinas en carrusel, con «Ideal para», modalidad (comodato/arriendo) y botón «Cotizar esta máquina». Comodato y arriendo se explican en dos tarjetas simples.
- Se eliminó la tabla de pedido mínimo por canal.
- Productos destacados del rubro (6) con ilustración, en lugar de los conteos por categoría.
- La franja «¿Todavía pides tu café por WhatsApp?» reemplaza la cita atribuida a una cafetería del piloto.
- **Formulario en dos pasos**: el paso 1 (nombre, correo, teléfono, tipo de negocio, región) registra la solicitud de cotización como lead, la asigna directo a Comercial (+25 en lead scoring) y avisa a marketing. El paso 2 (RUT, razón social, tamaño, máquina, crédito, clave) completa el mismo lead y crea la cuenta. «Ahora no, prefiero que me llamen» cierra sin perder el lead.
- «Conveniencia» pasa a «Estaciones de servicio y conveniencia» en los filtros.
- **Cinturón de confianza** bajo la primera pantalla (recomendación del profesor), con cifras del brief: 14 años en Chile (desde 2012), cerca de 4.000 máquinas, 3.390 puntos activos, N.º 1 en café en grano en supermercados (FNE), cobertura de la macrozona norte a la zona centro-sur y tipos de clientes. No se muestran logos porque el brief no nombra clientes reales.
- **Boletín Marley B2B** (antes del pie de página) para nurturing de quienes aún no cotizan: correo, tipo de negocio y consentimiento. Cada suscripción entra a la vista marketing como lead de contenidos con la etiqueta «Boletín», y se suma la automatización «Boletín mensual B2B».

**Portal**
- Inicio del cliente: la reposición sugerida va primero; los cuatro recuadros de texto pasan a una tarjeta «Tu consumo» con indicadores e histograma de gasto de 6 meses. Las cuentas nuevas ven una barra de avance de sus tres primeros pasos.
- Preguntas frecuentes (cliente, marketing y administrador) en tarjetas con más espacio.
- Marketing y administrador: cada tarjeta lleva un color según su tema (verde ventas y metas, amarillo leads y campañas, rojo alertas, café satisfacción). Rendimiento por canal, leads por origen, resultados por plataforma y evolución mensual se muestran como gráficos, con la tabla detallada plegable. Las automatizaciones muestran apertura y conversión como barras. En celular, la tabla de metas y la de presupuesto se leen como tarjetas.

## Usuarios de prueba
- Clientes: el RUT de cada cuenta demo (se ven en la pantalla de ingreso).
- Marketing: `marketing@marleycoffee.cl`
- Administrador (jefaturas): `admin@marleycoffee.cl`
- Clave de todas las cuentas de prueba: `marley2026`

## Rutas útiles para pruebas
- `index.html#/empresas` (general) y `#/empresas/oficinas`, `/horeca`, `/panaderias`, `/conveniencia`
- `#/ingresar` (login) · `#/privacidad` (política)
- `#/marketing/dashboard|leads|campanas|cuentas|ayuda` (vista marketing)
- `#/admin/resumen|operacion|clientes|campanas|reportes|ayuda` (vista administrador)
- `?utm_source=linkedin|meta|google` registra el origen del lead.

## Fotos pendientes
La franja de WhatsApp usa la foto del mesón (incrustada en `index.html`; originales en `imagenes/meson-800.webp` y `imagenes/meson-1600.webp`). Productos y máquinas usan ilustraciones. Para poner fotos, completa `PRODUCT_IMG` (por id de producto) y `MACHINE_IMG` (por id de máquina) en `index.html` con la ruta de cada imagen.

## Antes de publicar
Quitar el botón «Vistas del prototipo» y el botón «Completar con datos de prueba»,
conectar registro y login a un backend real y revisar legalmente la política de datos.
