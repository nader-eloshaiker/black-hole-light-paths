# Black Hole Light Paths

An interactive, ray-traced visualisation of why you can see the *back* of a black hole's accretion disk.

**Live page:** https://nader-eloshaiker.github.io/black-hole-light-paths/

## What it shows

- **What you see (left):** every pixel is a light ray traced backwards from your eye through the curved space around a non-spinning (Schwarzschild) black hole, running live on the GPU with WebGL.
- **Side view (right):** a cross-section along the centre line of the picture, showing the actual paths the light takes from the disk to you, with animated photons.

Light paths are colour-coded:

| Colour | Path |
| --- | --- |
| Orange | Near side of the disk, almost straight to you |
| Blue | Far side, top surface, bent **over** the hole |
| Pink | Far side, bottom surface, bent **under** the hole |
| Green | Light that wrapped around the hole (photon ring) |
| Grey | Rays that fall in: the black shadow |

## Controls

- **Viewing angle** from 0° (exactly edge-on) to 90° (looking straight down), or press *Sweep the angle*.
- **Gravity strength** from 0% (straight-line light) to 100% (real physics).
- **Colour the picture by light path** and **Doppler brightening** toggles.

## Physics and simplifications

Photon paths follow the Schwarzschild orbit equation, integrated as `x'' = -1.5 h² x / r⁵` (units of the event-horizon radius). The disk spans 3 to 12 horizon radii and is infinitely thin. Disk colours and texture are artistic; the Doppler option is an approximation.

## Running locally

It is a single self-contained HTML file. Open `black-hole-light.html` in any modern browser. No build step or server needed.
