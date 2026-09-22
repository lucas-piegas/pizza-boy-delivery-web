# Entrega Voladora — build web (PWA)

Sólo la **build web** del juego, para poder jugarlo desde el teléfono sin
instalar nada. El código vive en un repo aparte y privado.

**Jugar:** https://lucas-piegas.github.io/pizza-boy-delivery-web/

## Instalarlo en el iPhone

1. Abrir el enlace en **Safari** (no en Chrome: en iOS sólo Safari puede
   instalar aplicaciones web).
2. Botón de compartir → **Añadir a pantalla de inicio**.
3. Queda con su ícono y se abre a pantalla completa, sin la barra del navegador.
4. Poner el teléfono **apaisado**: el juego está pensado así.

La primera carga baja unos 40 MB (el motor). Después el *service worker* lo deja
guardado y abre al instante, incluso sin conexión.

## Cómo se regenera

Desde el repo del código:

    godot --headless --path . --export-release "Web" builds/web/index.html

El preset `Web` va **sin hilos** a propósito: la variante con hilos exige las
cabeceras COOP/COEP, que GitHub Pages no deja configurar.
