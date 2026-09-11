# MLE Group 1 – Prosit 1

Jupyter-based analysis of Ghana malaria data.

## Setup

Requires [uv](https://docs.astral.sh/uv/) (`brew install uv`).

```sh
git clone https://github.com/ASU-MICS-2028/mle-group-1-prosit-1.git
cd mle-group-1-prosit-1
uv venv --python 3.12
uv pip install -r requirements.txt
```

## Data

The `data/` folder is **never committed** (it is in `.gitignore`). Get it from a teammate
and place it at the repo root so the layout is:

```
data/
  raw/                 # source CSV / XLSX files
  ghana_boundaries/    # GeoJSON admin boundaries
  ...
```

## Run

```sh
source .venv/bin/activate
jupyter lab
```

Notebooks live in `notebooks/`. Load data with paths relative to the repo root, e.g. `../data/raw/...`.

## Adding a dependency

```sh
uv pip install <package>
```

then add it to `requirements.txt`.
