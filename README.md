[![kibot](https://github.com/nerdyscout/KiCAD-CICD-Template/actions/workflows/kibot.yml/badge.svg)](https://github.com/nerdyscout/KiBot-CICD-Template/actions/workflows/kibot.yml)

[![reuse](https://github.com/nerdyscout/KiCAD-CICD-Template/actions/workflows/reuse.yml/badge.svg)](https://github.com/nerdyscout/KiBot-CICD-Template/actions/workflows/reuse.yml)

---

# One-Inch-LaserDriver

...

## HowTo

Use this plugin to generate what's required for manufacturing with JLCPCB: https://github.com/Bouni/kicad-jlcpcb-tools

### KiBot

[KiBot](https://github.com/INTI-CMNB/KiBot/) is used to generate all kind of documentation from a KiCAD6 project.

Whenever a file matching `pcb/*.kicad_*` changes this workflow will trigger.

The following documents are generated on every build:

```
- pcb/cad/
   - dxf/
      - AutoCAD - DXF
   - boardview - BRD
   - 3D render - STEP
- pcb/docs/
   - bom/
      - Interactive BOM - HTML
      - Octopart list - CSV
      - KiCost - XLSX (disabled)
   - schematic - PDF
- pcb/img/
   - pcb/$fab/$style/
      - PCB top - SVG
      - PCB bottom - SVG
   - render/ (disabled)
      - PCB render - PNG
   - schematic - SVG
- pcb/gerbers - ZIP
```

### REUSE

Used to ensure every file got a propper license. 

## getting started

- [ ] PCB
   - [ ] change the filenames in `pcb/*.kicad_*` matching your repository name
   - [ ] create your PCB
- [ ] run `reuse --lint`
   - [ ] make sure the licenses of `pcb/*` fits your needs
- [ ] commit and push all those changes regulary to your project
