# MLE Group 1 – Prosit 1

Where should Ghana's limited bed nets go, and how confident can we be in the district-level estimates behind that decision?

Everything is in one notebook: [`notebooks/prosit1.ipynb`](notebooks/prosit1.ipynb). It runs top to bottom, from cleaning through the leakage audit to the allocation, and explains each step in plain language.

## Run it from a fresh clone

Requires [uv](https://docs.astral.sh/uv/) (`brew install uv`) and the `data/` folder from a teammate (see below).

```sh
git clone https://github.com/ASU-MICS-2028/mle-group-1-prosit-1.git
cd mle-group-1-prosit-1
uv venv --python 3.12 && uv pip install -r requirements.txt
# copy the data/ folder into the repo root, then:
.venv/bin/jupyter nbconvert --to notebook --execute --inplace notebooks/prosit1.ipynb
```

Or open it interactively with `.venv/bin/jupyter lab` and choose Run All. Takes about six minutes; section 15 runs 168 configurations.

## Layout

| Path | What |
|---|---|
| `notebooks/prosit1.ipynb` | The analysis, sections 1–15 (section 15 is the experiment matrix) |
| `notebooks/district_crosswalk.csv` | 2014–17 district names → 2021 boundary names (17 mismatches, 5 district splits) |
| `outputs/figures/`, `outputs/tables/` | Written by the notebook. Aggregates only, no household rows |

## Data

`data/` is **never committed** (it is in `.gitignore`): it contains a licensed DHS extract. Get it from a teammate and place it at the repo root:

```
data/
  ghana_district_cases.csv   ghana_mis_sample.csv   ghana_region_malaria.csv
  data_dictionary.md         # the datasheet
  ghana_boundaries/          # GeoJSON admin boundaries
  raw/                       # source CSV / XLSX files
```

The survey extract must not be uploaded to any generative-AI tool.

## Adding a dependency

`uv pip install <package>`, then add it with its version to `requirements.txt`.
