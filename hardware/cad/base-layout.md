# Base Layout — Rough CAD Blocks

Simplified footprints for blocking out `base.ipt`. All **mm**.

**Base plate:** 3 mm plywood · design on 305 × 305 stock · axle height **35** (wheel radius)

Last updated: 2026-07-08

---

## On the base (block these first)

| Part | Qty | Footprint (L × W) | Height ↑ | Radius / sweep | Notes |
|------|-----|-------------------|----------|----------------|-------|
| 70 mm omni wheel | 3 | **φ70** (R35) | axle at **35** from ground | **R38** min per corner | 3 mm shaft · [CAD](refs/omni-wheel-70mm/) |
| N20 motor + bracket | 3 | **30 × 45** mount plate | **18** body | **45** along axle | φ3 shaft · [CAD](refs/jga12-n20b/) |
| IBT-2 driver | 3 | **50 × 50** | **43** | — | one per wheel · [CAD](refs/ibt-2/) |
| Pi 5 + cooler | 1 | **85 × 56** | **32** | — | M2.5 standoffs · [CAD](refs/raspberry-pi-5/) |
| LiPo 2200 mAh | 1 | **110 × 40** | **28** | — | add 20 for T-plug end |
| Buck converter | 1 | **45 × 20** | **10** | — | ⚠️ measure yours |
| YDLIDAR X4PRO | 1 | **111 × 71** | **53** | **R60** clear at scan height | center top · [CAD](refs/ydlidar-x4pro/) |
| Pi camera | 1 | **25 × 24** | **12** | — | on gimbal post · ⚠️ confirm model |
| MG996R servo | 2 | **41 × 20** | **43** | — | pan + tilt · planned |

---

## By layer (top → bottom)

### Top deck (above main plate)
| Part | Block size | Stack height |
|------|------------|--------------|
| LiDAR | 111 × 71 | **53** |
| Gimbal post + camera | 50 × 50 base | **80–120** (estimate) |

### Main plate (electronics)
| Part | Block size | Stack height |
|------|------------|------|
| Pi 5 + cooler | 85 × 56 | **32** |
| 3× IBT-2 (side by side) | **150 × 50** total | **43** |
| Battery | 110 × 40 | **28** |
| Buck converter | 45 × 20 | **10** |

### Below / at plate edge (drive)
| Part | Block size | From ground |
|------|------------|-------------|
| Wheel (per corner) | **φ70** | center at **35** |
| Motor mount | 30 × 45 | plate ~**20–25** above ground |

---

## Minimum zones (cutouts / keep-clear)

| Zone | Size | Why |
|------|------|-----|
| Wheel corner ×3 | **φ75** each | roller overhang |
| LiDAR scan | **φ120** centered | 360° unobstructed |
| Pi USB / GPIO side | +**15** margin | cables |
| Wheel triangle | **120–150** between axle centers | 3-wheel omni starting point |

---

## Quick cylinders (Inventor primitives)

Use these if you aren't importing refs yet:

```
Wheel:     R35, thickness 35
Motor:     12 × 18 cross-section, length 40 along axle
Driver:    50 × 50 × 43 box
Pi stack:  85 × 56 × 32 box
LiDAR:     111 × 71 × 53 box
Battery:   110 × 40 × 28 box
Camera:    25 × 24 × 12 box
```

---

## CAD refs

| Part | Import file |
|------|-------------|
| Pi 5 + cooler | `refs/raspberry-pi-5/raspberry-pi-5-cooler.step` |
| Motor | `refs/jga12-n20b/jga12-n20b.sat` |
| LiDAR | `refs/ydlidar-x4pro/ydlidar-x4pro.step` |
| Driver | `refs/ibt-2/ibt-2.step` |
| Omni wheel | export `refs/omni-wheel-70mm/omni-wheel-70mm.step` from SW |

Full detail: [chassis-dimensions.md](../bom/chassis-dimensions.md)
