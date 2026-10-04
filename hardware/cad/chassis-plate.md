# Chassis plate cut files

Same hexagon as Inventor `chassis.ipt` / `chassis.dwg`, scaled up and cleaned for laser cut.

| File | Use |
|------|-----|
| `chassis-plate.dxf` | **Preferred** for most lasers |
| `chassis-plate.dwg` | AutoCAD / Inventor |
| `chassis-plate.svg` | Preview / Inkscape |
| `chassis.dwg` | Original Inventor export (small + sheet border) — keep as reference |

## Size

| | Original | Cut file |
|--|----------|----------|
| Bbox | 120 × 104 mm | **280 × 242.5 mm** |
| Scale | 1× | **2.33×** |
| Units | inches (on ANSI sheet) | **mm** |
| Border / title block | included | **removed** |

Fits **305 × 305 × 3 mm** birch plywood (~12 mm margin on the long side).

## Notes

- Outline only — no mounting holes yet (add after motor/Pi/LiDAR placement)
- Layer `CUT` in the DXF
- Origin ≈ plate centroid
