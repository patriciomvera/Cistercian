# Cistercian Numerals

A small, joyful project celebrating one of history's most elegant and forgotten number systems.

---

## What is this?

In the 13th century, Cistercian monks — bound by a vow of silence and running a network of over 500 monasteries across medieval Europe — devised a numeral notation so compact that **a single glyph could represent any integer from 1 to 9,999**.

No speech required. One mark. Done.

This is an interactive educational site that brings that system back to life: a live clock, a number converter, a full digit reference, and the historical context that makes it genuinely fascinating.

---

## The system

Every Cistercian numeral is built on a vertical stem divided into four spatial quadrants:

```
  ← Tens    │ Units →
  ───────────┼───────────
  ← Thousands│ Hundreds →
```

Each quadrant encodes one decimal digit (0–9) using a small vocabulary of line strokes. The quadrant determines the place value. Zero contributes nothing — the quadrant stays empty.

The result: one symbol, always the same size, regardless of whether the value is 1 or 9,999. Roman numerals needed up to 15 characters to express the same range. The Cistercian system always needs exactly one.

---

## Why it matters (beyond being beautiful)

What the monks built is, in modern terms, a **spatially encoded compression scheme**. Place value is embedded in geometry, not in the length of the token. This is the same principle behind QR codes, musical notation, and circuit diagrams.

They arrived at it in the 13th century.

The system was largely forgotten until historian **David A. King** spent a career reconstructing it, publishing his findings in *The Ciphers of the Monks* (Franz Steiner Verlag, 2001). After the Cistercians stopped using it, other groups adopted it as a cipher — its unfamiliarity became a feature.

---

## Features

- **Live Cistercian clock** — current hours, minutes and year rendered in the original notation, synced to your system time
- **Number converter** — type any number from 0 to 9,999 and see its glyph
- **Interactive builder** — compose a number digit by digit and watch each quadrant light up
- **Full reference table** — all 36 digit glyphs, clickable
- **Historical context** — the monks, the vow of silence, the information theory angle
- **The Anatomy of the Primes** (`primes.html`) — all 1,229 primes below 10,000 as a playable score (Web Audio), a "ghost" overlay of every glyph, a searchable matrix, and density charts. Every view can be compared against *all integers 1–9,999*. That comparison shows the prime signal lives almost entirely in the units quadrant (primes end in 1, 3, 7, 9), while the big wave in stroke density comes from the notation itself.

---

## Technical notes

Two HTML files (`index.html`, `primes.html`). No dependencies, no build step, no framework. Just a canvas renderer and some carefully placed strokes — which feels appropriate for a project about medieval monks who also believed in doing things simply.

The rendering engine mirrors the proportions of the historical glyphs:

```
  10% │ top padding
  20% │ upper digit area  (units / tens)
  40% │ bare stem — separation zone
  20% │ lower digit area  (hundreds / thousands)
  10% │ bottom padding
```

---

## Credits

Inspired by the Numberphile video on Cistercian numerals and the original research of David A. King.

Built for fun by **Patricio Vera**, with an AI collaborator who got a little too excited about medieval compression algorithms.

---

*"One written mark, and the recipient knows the exact page, year, or quantity — no speech required."*
