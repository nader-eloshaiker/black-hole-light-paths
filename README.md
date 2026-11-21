# Black Hole Light Paths

[![Live demo](https://img.shields.io/badge/demo-live-ffb25e?style=flat-square)](https://nader-eloshaiker.github.io/black-hole-light-paths/)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue?style=flat-square)](LICENSE)
[![Pages](https://img.shields.io/github/deployments/nader-eloshaiker/black-hole-light-paths/github-pages?label=pages&style=flat-square)](https://github.com/nader-eloshaiker/black-hole-light-paths/deployments)

An interactive, ray-traced simulation that answers one question: **why can you see the back of a black hole's accretion disk?**

**▶ Try it: https://nader-eloshaiker.github.io/black-hole-light-paths/**

![Ray-traced black hole beside a diagram of the curved light paths](assets/social-preview.png)

## What it shows

- **What you see (left).** Every pixel is a light ray traced backwards from your eye through the curved space around a non-spinning (Schwarzschild) black hole. It runs live on your GPU with WebGL.
- **Side view (right).** A cross-section along the centre line of the picture, showing the real paths light takes from the disk to you, with animated photons.

The light paths are colour-coded:

| Colour | Path |
| --- | --- |
| Orange | Near side of the disk, almost straight to you |
| Blue | Far side, top surface, bent **over** the hole |
| Pink | Far side, bottom surface, bent **under** the hole |
| Green | Light that wrapped around the hole (the photon ring) |
| Grey | Rays that fall in: the black shadow |

## Controls

- **Viewing angle** from 0° (exactly edge-on) to 90° (looking straight down), or press *Sweep the angle*.
- **Gravity strength** from 0% (light travels in straight lines) to 100% (real physics).
- **Colour the picture by light path** to match regions of the image to their paths.
- **Doppler brightening** to see the side of the disk moving towards you glow brighter.
- **Time dilation**: drag a probe clock around the black hole in the side view and compare it with clocks on the disk and at the photon sphere.

## The physics

Photon paths follow the Schwarzschild orbit equation, integrated numerically as

```
x'' = -1.5 · h² · x / r⁵
```

in units of the event-horizon radius, where `h` is the photon's specific angular momentum. This reproduces the photon sphere at 1.5 horizon radii and a shadow of about 2.6 horizon radii.

Time dilation uses the same geometry. A clock hovering at distance `r` runs at `√(1 − rₛ/r)` of the distant observer's rate, and a clock orbiting with the disk at `√(1 − 3rₛ/2r)`. Photons in the side view are timed by the distant observer's clock, using the exact Schwarzschild coordinate speed of light, so they visibly slow near the hole (the Shapiro delay).

Simplifications: the black hole does not spin, the disk spans 3 to 12 horizon radii and is infinitely thin, the disk colours and texture are artistic, and the Doppler option is an approximation.

## Running locally

It is a single self-contained page with no build step and no dependencies. Clone the repo and open `index.html` in any modern browser:

```bash
git clone https://github.com/nader-eloshaiker/black-hole-light-paths.git
open black-hole-light-paths/index.html
```

## Contributing

Bug reports, physics corrections and ideas are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[MIT](LICENSE) © 2026 Nader Eloshaiker

## Privacy

The live site counts visits with [GoatCounter](https://www.goatcounter.com/), which sets no cookies and collects no personal data, so no consent banner is needed. See the [privacy notice](https://nader-eloshaiker.github.io/black-hole-light-paths/privacy.html).
