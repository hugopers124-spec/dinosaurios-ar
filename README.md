# Dinosaurios AR

Experiencia de realidad aumentada hecha con **A-Frame 1.5.0** y **MindAR 1.2.5**. La página reconoce dos tarjetas y muestra un modelo 3D distinto sobre cada una:

| Tarjeta | Objetivo | Modelo 3D |
|---|---|---|
| `marcador.png` | 0 | Dinosaurio (`dinosaurio.glb`) |
| `marcador-escudo.png` | 1 | Escudo de hueso (`escudo.glb`) |

Página publicada: https://hugopers124-spec.github.io/dinosaurios-ar/

## Archivos

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La página de realidad aumentada |
| `targets.mind` | Las dos tarjetas compiladas para MindAR (0 = dinosaurio, 1 = escudo) |
| `marcador.png`, `marcador-escudo.png` | Las imágenes que reconoce la cámara: imprímelas o ábrelas en otra pantalla |
| `dinosaurio.glb` | Modelo 3D del dinosaurio, optimizado de 30.5 MB a 3.9 MB |
| `escudo.glb` | Modelo 3D del escudo, optimizado de 44.8 MB a 1.8 MB |

## Cómo probarlo

1. Abre la página desde una dirección **https** (por ejemplo, GitHub Pages). La cámara no funciona si abres el archivo directo desde la computadora.
2. Acepta el permiso de la cámara.
3. Apunta a una de las dos tarjetas, impresa o en otra pantalla. Se pueden ver las dos a la vez.

## Ajustes

En `index.html`, dentro de cada `<a-gltf-model>`:

- `scale`: tamaño del modelo. La tarjeta mide 1 de ancho.
- `position`: posición sobre la tarjeta (x, y, z).
- `rotation`: giro del modelo en grados (x, y, z).

Si agregas o cambias una tarjeta, hay que volver a compilar `targets.mind` con **todas** las imágenes, en el mismo orden, con el [compilador de MindAR](https://hiukim.github.io/mind-ar-js-doc/tools/compile). El orden define el número de objetivo (`targetIndex`).

GitHub Pages publica desde la rama `gh-pages`: después de cambiar `main`, actualiza también `gh-pages`.
