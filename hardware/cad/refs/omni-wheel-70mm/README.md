# 70 mm omni wheel reference model

MiJunHD 70 mm omni wheel with coupling (ordered ×3). For wheel clearance and axle layout in Inventor.

## Inventor import

| File | Inventor? | Use |
|------|-----------|-----|
| `omni-wheel-70mm.step` | **Yes** (best) | Export from `Omni_4_70.SLDASM` → full solid assembly |
| `omni-wheel-70mm-carrier.stl` | Yes (mesh) | Hub/carrier only — rough clearance check |
| `omni-wheel-70mm-roller.stl` | Yes (mesh) | Single roller — place 4× manually if needed |
| `Omni_4_70.SLDASM` | **No** | SolidWorks only — edit source, then export STEP |
| `*.SLDPRT` | **No** | SolidWorks only (gitignored) |

**Recommended workflow**
1. Open `Omni_4_70.SLDASM` in SolidWorks
2. **File → Save As → STEP** → save as `omni-wheel-70mm.step` in this folder
3. In Inventor: open `base.ipt` → **Place Component** → select `omni-wheel-70mm.step`

STL imports are triangle meshes — no precise mates. Use only until STEP is exported.

## Specs

**Dims:** φ70 × 35.4 mm wide · **3 mm** coupling bore · see [`part-photos/drive/omni-wheel.jpg`](../../bom/part-photos/drive/omni-wheel.jpg)

SolidWorks source files stay local (gitignored). Commit `omni-wheel-70mm.step` once exported.
