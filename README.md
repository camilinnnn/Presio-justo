# Precio Justo — MVP 0.2

Cotizador web estático para calcular costos y sugerir precios. No requiere servidor propio ni base de datos para las funciones locales.

## Publicar gratis con GitHub Pages

1. Inicia sesión en GitHub y crea un repositorio nuevo llamado `precio-justo`.
2. Elige **Public** y deja desmarcada la opción de agregar README (este paquete ya contiene uno).
3. Sube **el contenido** de este ZIP a la raíz del repositorio; el archivo `index.html` debe quedar directamente en la raíz, no dentro de otra carpeta.
4. Abre **Settings → Pages** y en **Build and deployment → Source** selecciona **GitHub Actions**.
5. En la pestaña **Actions**, espera a que termine el flujo `Deploy Precio Justo to GitHub Pages`.
6. La dirección será `https://TU-USUARIO.github.io/precio-justo/` (reemplaza `TU-USUARIO` por tu nombre de GitHub).

El flujo se ejecutará cada vez que actualices archivos en la rama `main`. La primera activación de Pages debe hacerse en Settings porque la integración no puede activar esa configuración por sí sola.

## Probar localmente

Puedes abrir `index.html` directamente para probar el cotizador. Para probar la instalación PWA y el modo sin conexión se requiere servirlo en HTTPS, como en GitHub Pages.

Si tienes Node.js instalado, ejecuta `node tests/verify.js` para las comprobaciones estáticas y casos de cálculo de referencia.

## Características

- Costos de materiales por unidad, cantidad fabricada, mano de obra, extras e indirectos.
- Precio sugerido a partir del margen, descuentos y redondeo.
- Catálogo local de materiales y respaldo JSON.
- Cotización para cliente sin exponer costos internos ni ganancia del vendedor.
- Copiar/compartir por WhatsApp e imprimir o guardar cotización como PDF.
- Archivos PWA: manifest, icono y service worker.

## Privacidad y limitaciones

La información permanece en el almacenamiento local de ese navegador/dispositivo; no hay cuentas, sincronización, backend ni envío de datos a un servidor. La fotografía del producto y el reconocimiento con IA aún no están implementados. Impuestos, comisiones, desperdicio y envío deben agregarse manualmente. Verifica importes y condiciones antes de enviar una cotización.
