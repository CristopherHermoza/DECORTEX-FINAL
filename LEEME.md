# DECORTEX — sitio web de cortinas y textiles

Sitio estático hecho con HTML, CSS y Bootstrap 5.3. No escribimos JavaScript propio:
las animaciones salen de los componentes de Bootstrap, que se activan con atributos
`data-bs-...` directamente en el HTML.

## Archivos

```
decortex/
├── index.html        Página principal (carrusel)
├── productos.html    Catálogo + ventana modal "Cómo medir tu ventana"
├── servicios.html    Proceso + acordeón de preguntas frecuentes
├── nosotros.html     Historia, valores y barras de progreso
├── contacto.html     Formulario y datos de contacto
├── css/
│   └── estilos.css   Estilos propios (se cargan DESPUÉS de Bootstrap)
└── img/              Aquí van tus fotos
```

Para verlo: abre `index.html` con doble clic. **Necesitas internet**, porque Bootstrap
se carga desde un CDN (jsDelivr).

## Las 5 animaciones (todas de Bootstrap)

| # | Animación | Dónde | Clase o atributo clave |
|---|-----------|-------|------------------------|
| 1 | Menú plegable de hamburguesa | Todas las páginas, en pantallas chicas | `navbar-toggler`, `data-bs-toggle="collapse"` |
| 2 | Carrusel con desvanecido | Inicio | `carousel carousel-fade`, `data-bs-ride="carousel"` |
| 3 | Acordeón | Servicios | `accordion`, `data-bs-parent` |
| 4 | Ventana modal con desvanecido | Productos | `modal fade`, `data-bs-toggle="modal"` |
| 5 | Barras de progreso con rayas en movimiento | Nosotros | `progress-bar-striped progress-bar-animated` |

Si el sistema del visitante tiene activada la opción de reducir movimiento, Bootstrap
desactiva las transiciones automáticamente.

## Qué cambiar primero

1. **Datos de contacto.** Busca `+51 900 000 000`, `hola@decortex.pe` y `Av. Ejemplo 123` en los cinco HTML.
2. **WhatsApp.** En `contacto.html` cambia `https://wa.me/51900000000` por tu número con código de país, sin `+` ni espacios.
3. **Porcentajes de Nosotros.** Los valores de las barras de progreso (95%, 90%, 88%) son de ejemplo. Cámbialos en `nosotros.html`, tanto el texto como `aria-valuenow` y `style="width: ..."`.
4. **Colores.** Están al inicio de `css/estilos.css`, dentro de `:root`.
5. **Fotos.** Los rectángulos con textura son marcadores (clase `.foto`). Cuando tengas imágenes, ponlas en `img/` y reemplaza `<div class="foto"></div>` por `<img src="img/sala.jpg" alt="Cortina blackout en sala">`.

## Sobre el formulario

El formulario de `contacto.html` todavía no envía nada. Para recibir los mensajes en tu correo, puedes usar un servicio como Formspree y poner la dirección que te den en el atributo `action` del `<form>`.

## Paleta y tipografía

Verde pino `#2c3a34`, salvia `#7d8f84`, arena `#e6e1d7`, hueso `#f8f7f4` y bronce `#9a7b4f` como acento. Títulos en Cormorant Garamond y texto en Karla (Google Fonts).
