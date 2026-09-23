This is a minimal example for using the expansion port.  We do not recommend using this for a real accessory, because of the rigid connection to the expansion port. But, it is a minimal reference for what could be done to interface with the expansion port.


Could install 1mm headers on top or bottom.

COPPER TOP side FACES USER 

Use:
 * 0.2mm holes
 * 0.1mm outside precision

REQUIREMENTS:
 * ENIG (prefer 2u) or Hard gold pads.
 * 0.8mm total thickness

Custom Notes:
 * You MUST chamfer edge connector.

IF NOT CHAMFERING:
 * 5x3 Panelization
 * Rails All 4 Sides
 * V-Cuts
 * 2mm Spacing between top and bottom.

IF CHAMFERING:
 * 5x2 Panelization
 * Rails All 4 Sides
 * V-Cuts
 * 2mm Spacing between top and bottom.



KiKit Recommended Configuration:
```json
{
    "layout": {
        "alternation": "rows",
        "vspace": "25mm",
        "vbonefirst": "2",
        "rows": "2",
        "cols": "5"
    },
    "cuts": {
        "type": "mousebites"
    },
    "framing": {
        "type": "railslr"
    }
}
```

```
kikit panelize^
    --layout "alternation: rows; vspace: 25mm; hbonefirst: 2; rotation: 180deg; rows: 2; cols: 5" ^
    --tabs "vwidth: 4.7mm; hwidth: 5mm; spacing: 15mm" ^
    --cuts "type: vcuts" ^
    --framing "type: railslr" ^
    "pcie-paddle-test.kicad_pcb" "outd.kicad_pcb"

```