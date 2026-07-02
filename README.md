# 📇 Generador de Código de Barras — DNI

Aplicación web que convierte un número de DNI en su **código de barras (Code 39)**, igual al que aparece en los documentos oficiales de datos del trabajador.

**➡ Ábrela aquí: https://rodrigo17312016-jpg.github.io/codigo-barras-dni/**

## ✨ Qué hace

| Función | Detalle |
|---|---|
| ⚡ Generación instantánea | Escribes el DNI y el código de barras aparece al momento |
| 🖱️ Copiar como **texto** | Selecciona las barras y cópialas: al pegar en Word aparece el **número** (igual que en el PDF original) |
| 🖼️ Copiar como **imagen** | Un clic y el PNG queda en el portapapeles, listo para pegar en Word/correo/WhatsApp |
| ⬇️ Descargar PNG | Imagen en alta resolución, escaneable |
| 📄 Modo Lote | Pega varios DNI (uno por línea) y genera una hoja imprimible |
| 🕘 Historial | Recuerda los últimos DNI usados (solo en tu navegador) |

## 🔍 Cómo funciona el truco de "copiar como texto"

El código de barras seleccionable se dibuja con la fuente **Libre Barcode 39** (embebida en el HTML): el contenido real del elemento **es el número**, solo que se *ve* como barras. Los caracteres de inicio/fin (`*`) del estándar Code 39 se añaden con pseudo-elementos CSS, por eso **se ven pero no se copian**.

La versión imagen se genera con [JsBarcode](https://github.com/lindell/JsBarcode) en un canvas de alta resolución, con los caracteres de control incluidos para que sea **escaneable**.

## 🛠️ Tecnología

- Un solo `index.html` — sin build, sin frameworks, sin dependencias externas en tiempo de ejecución.
- Fuente Libre Barcode 39 embebida en base64 (~4 KB) → funciona **sin conexión**.
- JsBarcode 3.11.6 incluido localmente en `vendor/`.

## 📜 Licencias

- [JsBarcode](https://github.com/lindell/JsBarcode) — MIT.
- [Libre Barcode 39](https://fonts.google.com/specimen/Libre+Barcode+39) — SIL Open Font License 1.1.
