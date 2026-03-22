# GreenTech-MVP-Sostenible_AngelLuis_SanchezPerez

La versión original cargaba la librería completa de Bootstrap únicamente para usar unas pocas clases de utilidad (display-1, fw-bold, lead, btn, etc.). Lo he reemplazado por CSS propio específico para los elementos necesarios, reduciendo el peso de la hoja de estilos.

Se cargaba la librería completa de iconos de Font Awesome para usar un único icono. Lo he sustituido por un emoji (🌱), que no requiere ninguna descarga adicional y tiene un impacto en red prácticamente nulo.

La fuente Montserrat se importaba con 5 pesos tipográficos (100, 300, 400, 700, 900), generando múltiples peticiones innecesarias a Google Fonts. Lo he reducido a solo 2 pesos (400 y 700), los únicos realmente usados en la página.

La imagen de fondo se solicitaba con un ancho de w=3000 píxeles. Lo he reducido a w=1200, suficiente para la mayoría de pantallas, lo que supone una notable reducción del tamaño del archivo descargado sin pérdida visual apreciable.

He creado clases CSS personalizadas (titulo-principal, texto-lead, btn-eco) que reemplazan las clases de utilidad de Bootstrap. Esto elimina la necesidad de cargar un framework entero y hace el código más legible y mantenible.

El footer original no existía en el HTML, era generado dinámicamente mediante JavaScript con jQuery ($("body").append(...)). Al tratarse de contenido completamente estático (solo varía el año), he declarado directamente en el HTML, eliminando así una dependencia de JavaScript y mejorando el rendimiento de carga.
