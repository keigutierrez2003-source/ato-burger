# A'TO Burger — Valledupar

Página del menú de A'TO Burger, comidas rápidas en Villa Taxi, Valledupar (Cesar).

**Mz S casa 6, Villa Taxi** · Viernes, sábado y domingo de 6:00 PM a 11:00 PM

## Qué hace

Sitio estático de una sola página. El cliente arma su pedido desde el menú y lo envía
por WhatsApp con el resumen, los precios y sus notas ya redactados.

- Menú por categorías: hamburguesas, perros, salchipapas, combos, adicionales y bebidas.
- Carrito que guarda el pedido en el navegador aunque se cierre la pestaña.
- Indicador de abierto/cerrado calculado en hora de Colombia.
- Adaptado a celular, tablet y computador.

## Estructura

```
index.html      Toda la página: estructura, estilos y lógica en un solo archivo
img/            Fotos de los productos (AVIF), logotipo y favicon
Menú.txt        Menú de referencia con precios
MenúATO.jpeg    Afiche original del menú
```

## Cómo cambiar el contenido

Todo lo editable está al inicio del bloque `<script>` en `index.html`.

**Datos del negocio** — objeto `CONFIG`: número de WhatsApp, dirección, horario,
días de apertura y redes sociales.

**Productos** — arreglo `MENU`. Cada categoría tiene sus items con nombre, precio,
descripción, foto y etiqueta. Agregar o quitar un producto ahí actualiza toda la
página: las tarjetas, el contador de la categoría y el carrito.

Las fotos van en `img/` en formato `.avif` y se referencian sin la extensión
(por ejemplo `img/ATOclasica`).

## Publicación

Sitio estático, sin dependencias ni proceso de compilación. Se despliega solo en
Vercel con cada push a `main`.

Para verlo en local:

```bash
python -m http.server 8123
```
