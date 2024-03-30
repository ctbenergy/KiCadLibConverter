# KiCadLibConverter

Devcontainer for [easyeda2kicad](https://github.com/uPesy/easyeda2kicad.py) and [JLC2KiCad_lib](https://github.com/TousstNicolas/JLC2KiCad_lib).

## easyeda2kicad

[easyeda2kicad](https://github.com/uPesy/easyeda2kicad.py)

A Python script that converts any electronic components from EasyEDA or LCSC to a Kicad library including 3D model in color. T

### Usage

```bash
# For symbol + footprint + 3d model (with --full argument)
easyeda2kicad --full --lcsc_id=C2040
# For symbol + footprint + 3d model
easyeda2kicad --symbol --footprint --3d --lcsc_id=C2040
# For symbol + footprint
easyeda2kicad --symbol --footprint --lcsc_id=C2040
# For symbol only
easyeda2kicad --symbol --lcsc_id=C2040
# For footprint only
easyeda2kicad --footprint --lcsc_id=C2040
# For 3d model only
easyeda2kicad --3d --lcsc_id=C2040
# For symbol in Kicad v5.x legacy format
easyeda2kicad --symbol --lcsc_id=C2040 --v5
```

Default output folder
```bash
~/Documents/Kicad/easyeda2kicad
3dshapes
~/Documents/Kicad/easyeda2kicad/easyeda2kicad.3dshapes
footprints
~/Documents/Kicad/easyeda2kicad/easyeda2kicad.pretty
symbol file
~/Documents/Kicad/easyeda2kicad/easyeda2kicad.kicad_sym
```

Example usage:

```bash
easyeda2kicad --full --lcsc_id=C2040
```

For output folder see devcontainer.json mounts.

## JLC2KiCad_Lib

[JLC2KiCad_lib](https://github.com/TousstNicolas/JLC2KiCad_lib)

### Usage

Example usage:

```bash
JLC2KiCadLib C475120 \
-dir ~/Documents/Kicad/JLC2KiCadLib/ \
-model_dir JLC2KiCadLib.3dshapes \
-footprint_lib JLC2KiCadLib.pretty   \
-symbol_lib_dir / \
-symbol_lib JLC2KiCadLib.kicad_sym
```

For output folder see devcontainer.json mounts.

## REQUIREMENTS
Visual Studio Code Dev Containers: <https://code.visualstudio.com/docs/devcontainers/containers#_system-requirements>
