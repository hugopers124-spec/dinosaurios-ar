# Dinosaurios AR

Experiencia de realidad aumentada hecha con **A-Frame 1.5.0** y **MindAR 1.2.5**. Al apuntar la cámara del celular a la imagen `marcador.png`, aparece un dinosaurio en 3D sobre ella.

## Archivos

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La página de realidad aumentada |
| `targets.mind` | El marcador compilado para MindAR (sale de `marcador.png`) |
| `marcador.png` | La imagen que reconoce la cámara: imprímela o ábrela en otra pantalla |
| `dinosaurio.glb` | El modelo 3D, optimizado de 30.5 MB a 3.9 MB |

## Cómo probarlo

1. Abre la página desde una dirección **https** (por ejemplo, GitHub Pages). La cámara no funciona si abres el archivo directo desde la computadora.
2. Acepta el permiso de la cámara.
3. Apunta al `marcador.png`, impreso o en otra pantalla.

## Ajustes

En `index.html`, dentro de `<a-gltf-model>`:

- `scale`: tamaño del dinosaurio. La tarjeta mide 1 de ancho.
- `position`: posición sobre la tarjeta (x, y, z).
- `rotation`: giro del modelo en grados (x, y, z).

Si cambias la imagen del marcador, hay que volver a compilar `targets.mind` con el [compilador de MindAR](https://hiukim.github.io/mind-ar-js-doc/tools/compile).
