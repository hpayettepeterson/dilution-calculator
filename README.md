# Spinout dilution & protection calculator

An interactive tool for modelling how a university's equity stake in a spinout survives dilution across funding rounds — and what an anti-dilution-protected stake is actually worth in plain, fully-dilutable terms.

**Live:** https://hpayettepeterson.github.io/dilution-calculator/

Companion to the [equity equivalence calculator](https://hpayettepeterson.github.io/equity-calculator/). Where that tool compares a single protected stake against a dilutable one across exit sizes, this one lets you build and compare **arbitrary, fully-editable funding scenarios**.

## What it does

- **Edit every round** — add, remove, or rename rounds and set pre-money and amount raised. Post-money, per-round dilution, and the running stake are computed live.
- **Four anti-dilution protection modes:**
  - *No protection* — ordinary dilutable equity.
  - *Post-money cap* — protected in any round whose post-money ≤ the cap.
  - *Cumulative raised cap* — protected while total equity raised ≤ the cap.
  - *Through round* — protected up to and including a chosen round.
- **Equivalence** — the headline number: the starting % of an ordinary, fully-dilutable stake that lands on the same final % after all rounds. This is what the protection is "worth" at incorporation.
- **Save & compare scenarios** — snapshot any setup, name it, and compare final stake, equivalent dilutable stake, and value at exit side by side, with a chart.
- **EUR / USD toggle** with an editable FX rate.

Everything runs in the browser. Edits and saved scenarios persist in `localStorage` on your device only — nothing is uploaded.

## Reference case

The default rounds are a European deep-tech / life-science spinout path through Series D, based on PitchBook, Carta, Atomico, and SVB Healthcare 2024–2025 medians. "Reset to reference case" restores them. Sources are listed in-app.

## Run locally

It's a single static `index.html` — open it directly, or serve the folder:

```bash
npx serve .
```

## Stack

Plain HTML / CSS / vanilla JS. [Chart.js](https://www.chartjs.org/) (CDN) for the comparison chart. No build step.
