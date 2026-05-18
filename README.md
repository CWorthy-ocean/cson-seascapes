# cson-views

Visualizations of the C-Star Ocean Network — a global collection of regional
and basin-scale ROMS configurations supported by the [C-Star](https://github.com/CWorthy-ocean/C-Star)
reproducible workflow framework.

![C-Star Ocean Network domains](cson-map.png)

Each rectangle delineates a ROMS grid configuration on a global Robinson
projection. Perimeter color denotes the validation state of the
configuration:

- **tab:blue — Scientifically validated:** the configuration's ocean (and
  biogeochemical, where applicable) solution has been evaluated against
  observations.
- **tab:orange — Functionally validated:** the configuration runs end-to-end
  and produces a stable solution, but has not yet been scientifically
  validated.
- **tab:purple — Illustrative of potential extensions to the network:**
  candidate domains whose geometries are defined here but which are not yet
  configured.

All domains shown are supported by the C-Star reproducible workflow
framework, which enables users to build and operate any of these models on
a supported machine.

## Files

- `grids.yml` — grid configurations (geometry + validation state) for every
  domain in the network.
- `cson_map.ipynb` — builds each grid via `roms_tools` and renders the map.
- `cson-map.png` — current rendered figure.

## Running

The notebook depends on `roms_tools`, `cartopy`, `cmocean`, `pyyaml`, and
`matplotlib`. Open `cson_map.ipynb` and run all cells.
