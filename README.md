# data-generation
# SyntheticGen

![CI](https://github.com/OtKwesi/SyntheticDataGen_project/actions/workflows/ci.yml/badge.svg)
![License](https://img.shields.io/github/license/OtKwesi/SyntheticDataGen_project)
![Python](https://img.shields.io/badge/python-3.10%2B-blue)

Generate custom synthetic datasets for ML & data science from simple YAML schemas — fast, local, and privacy-safe.

---

## 🚀 Quickstart (30 seconds)

### Install (dev / local)
```bash
git clone https://github.com/OtKwesi/SyntheticDataGen_project.git
cd SyntheticDataGen_project
python -m pip install -e .

from syntheticgen import generate_synthetic_data

df = generate_synthetic_data("schemas/example.yaml", n_rows=50, save_csv=True, filename="sample.csv")
print(df.head())
