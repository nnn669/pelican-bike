# 🐦 Pelican Riding a Bicycle

A 2D animation of a pelican riding a bicycle, drawn entirely with **SVG** + CSS animations.

## Live demo

👉 **https://nnn669.github.io/pelican-bike/**

## What's inside

| Part | Technique |
|---|---|
| Wheels spinning | `<animateTransform type="rotate">` |
| Chain + sprocket | dashed stroke with `stroke-dashoffset` keyframes |
| Background parallax | layered CSS `@keyframes` translateX (clouds / hills / trees / road dashes) |
| Wing flapping | `animateTransform` rotate on a wing group |
| Pedaling legs | two-link **inverse kinematics** solved per frame in `requestAnimationFrame` |

The far leg is painted behind the bike frame and the near leg in front, so the
occlusion looks right. Neck, head and beak bob in sync with the wing beat.

`prefers-reduced-motion` is respected — the scene freezes on a static pose.

## Run locally

```sh
python3 -m http.server 8000
# then open http://localhost:8000
```

Single file, zero dependencies.
