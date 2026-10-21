# Population Genetics Fishbowl — Independent Teaching Simulation

Single-page, no-dependency HTML/JavaScript educational simulation for GitHub Pages. This is an independent implementation inspired by the broad educational concept of virtual population genetics fish tanks, not a reproduction of Virtual Biology Lab's source code or exact simulation behaviour.

## Installation

Upload `index.html` to the ROOT of a public GitHub repository. Under Settings → Pages, publish from branch `main` and folder `/ (root)`. The page will work offline when opened as an HTML file, too.

## Features

- Animated red (RR), pink (Rr), white (rr) fish under incomplete dominance.
- Adjustable population size, carrying capacity, allele frequency, relative genotype survival, migration, mutation, assortative mating and growth.
- Independent run/reset, step, +100 generations, continuously updated graphs.
- Raw student measurements captured from the *current* generation, shown on screen and exported to CSV.

## Scientific notes / limitations

This simplified independent model uses **discrete non-overlapping generations**. It is not a faithful clone of VBL's agent-based NetLogo lifecycle. The model targets population size via a density-dependent deterministic expected population, chooses eligible parents via genotype-specific survival, pairs fish using genotype-similarity weighting, generates offspring by Mendelian segregation, mutates each gametic allele, and finally replaces some offspring with migrants. A visual fish position does not influence reproduction. No Allee effect, sex ratio, age structure, explicit spatial mating or stochastic mortality-driven extinction is modelled. Such features would be separate enhancements.

Unlike a literal Hardy-Weinberg ideal infinite population, this simulator has finite N, so genetic drift continues under neutral settings. For reproducibility, seed-based PRNG could be added in a subsequent release. No student data is transmitted or collected centrally.
