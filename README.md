# Script de Wallpapers Animados con Pywal y Mpvpaper
----------------------------------------------------

Este script permite aplicar fondos de pantalla en Linux usando pywal y mpvpaper.
Soporta imágenes y videos (extrae un frame para la paleta de colores y reproduce el video con mpvpaper).

## Dependencias

Instalar dependencias en Arch Linux con yay:

yay -S python-pywal16 ffmpeg mpvpaper

## Instalación del script

Copiar el script a ~/.local/bin y darle permisos de ejecución:

mkdir -p ~/.local/bin
cp awal ~/.local/bin/awal
chmod +x ~/.local/bin/awal

Asegurarse de que ~/.local/bin esté en tu PATH:

echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc

Instalación completada.

## Uso

Para aplicar una imagen:

awal -i /ruta/a/imagen.jpg

Para aplicar un video:

awal -v /ruta/a/video.mp4

## Notas

- El script crea un frame temporal en ~/.cache/wal/animated/frame.png
- Para detener un video animado: pkill mpvpaper
