# ☠ Zombie percolation — the tipping point at 59.27 %

<p>
  <a href="https://technikweber.github.io/percolation-theory-simulator/"><img alt="Live demo" src="https://img.shields.io/badge/live%20demo-open-brightgreen"></a>
  <img alt="Runs in the browser" src="https://img.shields.io/badge/runs%20in-the%20browser-blue">
  <img alt="UI language: German" src="https://img.shields.io/badge/UI-Deutsch-informational">
  <a href="LICENSE"><img alt="License: MIT" src="https://img.shields.io/badge/license-MIT-green"></a>
</p>

An interactive browser simulation in Minecraft style that makes one of the most
fascinating effects in mathematics visible: the **phase transition** of percolation
theory. Plain HTML, CSS and JavaScript — no back end, nothing to install.

👉 **[Try it](https://technikweber.github.io/percolation-theory-simulator/)**

## What it is about

Scatter people randomly across a map. A single one turns into a zombie and infects
everyone standing right next to them. Whether humanity survives depends only on the
**population density** — and on a razor-sharp threshold:

- **Just below ≈ 59.27 %:** the population breaks into many small, isolated islands. A
  bite stays locked in locally → humanity survives.
- **Just above:** all of a sudden one giant connected cluster spans the whole map. A
  single bite sets off a chain reaction → apocalypse.

This jump from "perfectly safe" to "total escalation" is a **phase transition** (tipping
point) — the same mathematical phenomenon behind uncontrollable forest fires, exploding
epidemics and system collapses such as the 2008 financial crisis.

## The mathematics behind it

This is **site percolation** on a square lattice with a 4-neighbourhood. Each cell is
occupied with probability `p`; the infection only spreads along directly connected
neighbours.

The critical threshold is:

```
p_c ≈ 0.592746…
```

The striking part: this value shows up in **every** computer simulation and has been
measured with high precision — yet to this day **nobody has derived it with an exact,
closed formula**. That makes it one of the great open puzzles.

## Features

- **Interactive map** — people are placed randomly at an adjustable density
- **Slider** with the critical threshold at 59.27 % marked
- **Start an outbreak** by clicking a person or with a random bite
- **Animated spread** of the infection along connected neighbours
- **Live situation report** — population, number infected, share and verdict
  (survival / apocalypse)
- **Experiment mode** — builds the S-curve of percolation probability against density and
  shows how the transition sits exactly at 59.27 %
- Three map sizes (40×40 to 80×80)

## Controls

| Action | Effect |
|---|---|
| **Slider** | Set the population density |
| **Click on a person** | Start the outbreak exactly there |
| **Ausbruch!** (outbreak) | Bite at a random spot |
| **Heilen** (heal) | Reset the infection |
| **Neu generieren** (regenerate) | Roll a new map |
| **Experiment starten** | Calculate the threshold curve |

Tip: move the density from 57 % to 61 % and start an outbreak each time — the difference
between a local incident and complete extinction is striking.

The interface is in German.

## Run it locally

```bash
git clone https://github.com/TechnikWeber/percolation-theory-simulator.git
```

Then open `index.html` in a browser. The pixel fonts need an internet connection (Google
Fonts).

## Technology

- HTML5 canvas for the grid and the chart
- Vanilla JavaScript (flood fill / iterative depth-first search for the clusters)
- CSS with pixel fonts (Press Start 2P & VT323)

## Source and further reading

Alemi, Alexander A., et al. *"You can run, you can hide: The epidemiology and statistical
mechanics of zombies."* Physical Review E **92**.5 (2015): 052801.

## License

[MIT](LICENSE).
