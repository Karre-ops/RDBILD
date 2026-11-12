# RDBILD – Bildbetrachter für RetroDesk 2

RDBILD.EXE zeigt BMP, PCX, GIF und JPEG (Baseline, verkleinert 1/2 bis 1/8) unter RetroDesk 2, mit Rasterung für Bildschirme mit wenigen Farben und Lage aus Exif.

## Installation
`RDBILD.EXE` in den RD2-Ordner kopieren (z. B. `C:\RD2`). Die RD2-Shell öffnet BMP, PCX, GIF und JPG dann per Doppelklick damit.

## Bauen
Quellen in `src/`. Gebaut wird im RetroDesk-2-Baum (github.com/Karre-ops/RetroDesk2) mit Open Watcom:
`src/` nach `apps/bild/` kopieren, dann in `build.sh`:
```
APPOBJ=",obj/bk_BLESER.obj,obj/bk_JPEG.obj" app apps/bild/RDBILD.C RDBILD.EXE "Bild"
```
Test: `test/rdbild.sh`.

Lizenz: GPL v2 oder später (siehe COPYING).
