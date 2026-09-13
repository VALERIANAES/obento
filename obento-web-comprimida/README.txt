OBENTO — CARTA DIGITAL (solo consulta, sin pedidos online)
=============================================================

Esta web ya NO permite hacer pedidos desde el navegador. Es solo
una carta digital bonita para que el cliente vea los platos, fotos,
precios y alérgenos — el pedido se hace SIEMPRE por teléfono. Por
eso ya no hay carrito, ni pago, ni impresión automática, ni
Firebase: todo eso se ha quitado porque ya no hace falta.

MUY IMPORTANTE — pon tu teléfono real
-------------------------------
Abre js/menu-data.js, busca "telefono:" (dentro de ABOUT_INFO) y
pon tu número real, con el formato +34 6XX XXX XXX. Ese número es
el que aparece en el botón grande de "Pide por teléfono" de toda
la web (splash, carta y ubicación) — ahora mismo tiene un número
de ejemplo.

Cómo abrir la previsualización
-------------------------------
Haz doble clic en "index.html" y se abre en el navegador. No hace
falta servidor ni instalar nada.

Qué archivo tocar para cada cosa
-------------------------------
- Añadir, quitar o editar PLATOS, PRECIOS o FOTOS
  -> js/menu-data.js   (es el único archivo pensado para tocar a diario)

- Cambiar FOTOS de los platos
  -> pon el archivo dentro de la carpeta images/ con el nombre EXACTO
     que aparece en el campo "imagen" de cada plato en js/menu-data.js
     (ej: images/edamame.jpg)

- Cambiar textos de "Conócenos" y "Ubicación", dirección, horario, teléfono
  -> también en js/menu-data.js (objeto ABOUT_INFO, al final del archivo)

- Cambiar COLORES o el DISEÑO visual
  -> css/styles.css (los colores principales están arriba del todo,
     dentro de ":root"). Ahora mismo el tema es negro con rojo y
     blanco/crema, como se pidió.

- Tipografía del logo "OBENTO" (estilo Edo)
  -> pon el archivo de la fuente en fonts/Edo.woff2 (o .ttf). Ver
     fonts/README.txt.

- Navegación entre pantallas, carta, botones de llamar
  -> js/app.js (normalmente NO hace falta tocarlo)

Estructura de carpetas
-------------------------------
obento-carta/
  index.html          <- estructura de la app (splash, carta, conócenos, ubicación)
  css/styles.css       <- todo el diseño visual
  js/menu-data.js      <- EDITA AQUÍ: platos, precios, fotos, categorías, teléfono
  js/app.js            <- navegación y renderizado de la carta (sin pedidos)
  images/               <- pon aquí las fotos de los platos y el logo
  fonts/                <- pon aquí la fuente Edo si la vas a usar

Publicar la web
-------------------------------
Sigue funcionando igual que antes con Netlify: sube esta carpeta
completa (arrastrándola) a tu sitio en Netlify, sin necesidad de
nada más — ya no hace falta configurar variables de entorno,
funciones, Firebase, PrintNode ni Stripe, todo eso se ha quitado.
