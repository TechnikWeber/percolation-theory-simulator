# ☠ Zombie-Perkolation — Der Kipppunkt bei 59,27 %

Eine interaktive Browser-Simulation in Minecraft-Optik, die einen der faszinierendsten Effekte der Mathematik sichtbar macht: den **Phasenübergang** der Perkolationstheorie. Komplett in HTML, CSS und JavaScript – kein Backend, keine Installation.

## 🧟 Live-Demo

👉 **[Hier ausprobieren](https://technikweber.github.io/percolation-theory-simulator/)**

Einfach den Link öffnen – die Simulation läuft direkt im Browser.

> *(Den Link an den tatsächlichen Repo-Namen anpassen.)*

## Worum geht es?

Verteile Menschen zufällig auf einer Karte. Ein Einziger wird zum Zombie und infiziert jeden, der direkt neben ihm steht. Ob die Menschheit überlebt, entscheidet allein die **Bevölkerungsdichte** – und zwar an einer messerscharfen Grenze:

- **Knapp unter ≈ 59,27 %:** Die Bevölkerung zerfällt in lauter kleine, isolierte Inseln. Ein Biss bleibt lokal eingeschlossen → die Menschheit überlebt.
- **Knapp darüber:** Schlagartig entsteht ein einziger riesiger zusammenhängender Cluster, der die ganze Karte durchspannt. Ein einziger Biss löst eine Kettenreaktion aus → Apokalypse.

Dieser Sprung von „absolut sicher" zu „totale Eskalation" ist ein **Phasenübergang** (Tipping Point) – dasselbe mathematische Phänomen, das hinter unkontrollierbaren Waldbränden, explodierenden Epidemien und Systemkollapsen wie der Finanzkrise 2008 steckt.

## Die Mathematik dahinter

Das ist **Site-Perkolation** auf einem quadratischen Gitter mit 4er-Nachbarschaft. Jede Zelle ist mit Wahrscheinlichkeit `p` besetzt; die Infektion breitet sich nur entlang direkt verbundener Nachbarn aus.

Der kritische Schwellenwert liegt bei:

```
p_c ≈ 0,592746…
```

Das Verblüffende: Dieser Wert taucht in **jeder** Computersimulation auf, ist hochpräzise gemessen – aber bis heute konnte ihn **kein einziger Mathematiker durch eine exakte, geschlossene Formel herleiten**. Genau das macht ihn zu einem der großen offenen Rätsel.

## Funktionen

- **Interaktive Karte** – Menschen werden zufällig mit einstellbarer Dichte verteilt
- **Schieberegler** mit markierter kritischer Grenze bei 59,27 %
- **Ausbruch starten** per Klick auf einen Menschen oder per Zufallsbiss
- **Animierte Ausbreitung** der Infektion entlang verbundener Nachbarn
- **Live-Lagebericht** – Bevölkerung, Infiziertenzahl, Anteil und Verdikt (Überleben / Apokalypse)
- **Experiment-Modus** – baut die S-Kurve der Perkolations-Wahrscheinlichkeit gegen die Dichte auf und zeigt, wie der Übergang exakt bei 59,27 % sitzt
- Drei Kartengrößen (40×40 bis 80×80)

## Bedienung

| Aktion | Wirkung |
|---|---|
| **Schieberegler** | Bevölkerungsdichte einstellen |
| **Klick auf einen Menschen** | Ausbruch genau dort starten |
| **Ausbruch!** | Biss an zufälliger Stelle |
| **Heilen** | Infektion zurücksetzen |
| **Neu generieren** | Karte neu auswürfeln |
| **Experiment starten** | Schwellenwert-Kurve berechnen |

Tipp: Schieb die Dichte einmal von 57 % auf 61 % und starte jeweils einen Ausbruch – der Unterschied zwischen lokalem Vorfall und vollständiger Auslöschung ist verblüffend.

## Lokal ausführen

Reines Frontend – einfach klonen und die Datei im Browser öffnen:

```bash
git clone https://github.com/technikweber/Zombie-Perkolation.git
```

Dann `zombie-perkolation.html` (bzw. `index.html`) öffnen. Für die Pixel-Schriften wird eine Internetverbindung benötigt (Google Fonts).

## Technik

- HTML5 Canvas für das Gitter und das Diagramm
- Vanilla JavaScript (Flood-Fill / iterative Tiefensuche für die Cluster)
- CSS mit Pixel-Schriften (Press Start 2P & VT323)

## Quelle & mehr zum Thema

Alemi, Alexander A., et al. *„You can run, you can hide: The epidemiology and statistical mechanics of zombies."* Physical Review E **92**.5 (2015): 052801.

## Lizenz

*(z. B. MIT – nach Wunsch ergänzen)*
