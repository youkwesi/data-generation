# SyntheticDataGen_project
![Demo](demo.gif) <!-- Replace with actual GIF path or remove if not ready -->

## Badges
| CI Status | License | Python Version |
|-----------|---------|----------------|
| [![CI](https://github.com/OtKwesi/SyntheticDataGen_project/actions/workflows/ci.yml/badge.svg)](https://github.com/OtKwesi/SyntheticDataGen_project/actions) | [![License](https://img.shields.io/github/license/OtKwesi/SyntheticDataGen_project)](https://github.com/OtKwesi/SyntheticDataGen_project/blob/main/LICENSE) | [![Python](https://img.shields.io/badge/python-3.10%2B-blue)](https://www.python.org/downloads/) |

SyntheticGen is a plug-and-play synthetic data generator for machine learning engineers, data scientists, and analysts. It allows you to define your dataset schema in YAML and generate realistic synthetic datasets in CSV or Pandas DataFrame format.

The goal is to provide an open-source alternative to Kaggle datasets by letting you generate your own customizable data.

✨ **Features**
- Define datasets via simple YAML schemas.
- Generate CSV files or directly return Pandas DataFrames.
- Command-line interface (CLI) and Python API.
- Flexible: works for any project domain (ML, data analytics, data science).
- MIT Licensed — free to use, modify, and share.
- CI/CD ready with GitHub Actions and unit tests.

📦 **Installation - Quickstart (30 seconds)**
```bash
# Step 1: Clone the repository
git clone https://github.com/OtKwesi/SyntheticDataGen_project.git
cd SyntheticDataGen_project

# Step 2: Install dependencies
pip install -r requirements.txt

# Step 3: Install the package locally
pip install .

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

Python API
from syntheticgen import generate_synthetic_data

df = generate_synthetic_data("schemas/example.yaml", n_rows=50, save_csv=True, filename="sample.csv")
print(df.head())

CLI
# example
syntheticgen --schema schemas/example.yaml --rows 100 --out sample.csv

✨ Why use SyntheticGen?

Define schemas in YAML and produce realistic CSVs or Pandas DataFrames.

Great for testing ML pipelines, prototyping, and creating privacy-safe demo data.

Includes CLI, Python API, tests and CI.
🧩 Example YAML (schemas/example.yaml)
# columns: simple example
- name: id
  type: id
  prefix: U
- name: amount
  type: numeric
  range: [10, 5000]
- name: date
  type: datetime
  start_date: "2023-01-01"
  end_date: "2024-12-31"
- name: category
  type: categorical
  categories: ["A", "B", "C"]
- name: notes
  type: text
  faker: sentence

🧪 Running tests
# recommended
pip install -r requirements.txt
pytest tests/ --tb=short

📁 Project structure
syntheticgen_project/
├─ syntheticgen/        # package (generator, cli, utils)
├─ schemas/             # example YAML schemas
├─ tests/               # unit tests
├─ .github/workflows/   # CI
├─ setup.cfg
├─ pyproject.toml
└─ README.md

📣 Contributing & roadmap

Open issues for bugs or feature requests (e.g., parquet output, domain-specific faker profiles).

Want to help? Fork, open a PR and add tests.

📌 Release & install

I tag releases in GitHub (e.g., v0.1.0).

For now install with pip install -e . (editable). PyPI packaging coming soon.

⚖️ License

MIT — see LICENSE.

If this README is useful, please ⭐ the repo!

---

# 2) Replace the README using **VS Code** (recommended)

1. Open VS Code and the project folder.  
2. In Explorer, click `README.md`.  
3. Press `Ctrl+A` to select all, paste the new content (from the box above).  
4. Save: `Ctrl+S`.  
5. Commit & push:

```powershell
git add README.md
git commit -m "docs: revamp README with quickstart, badges and examples"
git push
