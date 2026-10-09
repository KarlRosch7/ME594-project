# ME594-project
Term project for Data Science ME 594. Creates a ML model to predict who should be screened for diabetes.

## Setup

1. Clone the repo:
   ```
   git clone https://github.com/KarlRosch7/ME594-project.git
   cd ME594-project
   ```
2. Create and activate the environment:
   ```
   uv venv --python 3.14
   ```
   - Windows: `.venv\Scripts\activate`
   - Mac/Linux: `source .venv/bin/activate`
3. Install packages:
   ```
   uv pip install -r requirements.txt
   ```
4. Turn on notebook output stripping (once per clone):
   ```
   nbstripout --install
   ```
   This removes cell outputs on commit so notebooks don't cause merge conflicts.

## Data

The data is **not** in git (too large). Download it from CDC BRFSS 2025 and place it so the paths look like:
```
../data/LLCP2025XPT/LLCP2025.XPT
../data/<your_file>.parquet
```
Source: CDC BRFSS 2025 (https://www.cdc.gov/brfss/annual_data/annual_data.htm).

## Working with notebooks

- Notebooks live in `notebooks/` and load data with relative paths, e.g. `pd.read_parquet("../data/<your_file>.parquet")`.
- Don't edit the same notebook at the same time. Git can't merge notebooks cleanly. Each of us works in our own notebook or we agree on who edits which.
- Put reusable code (cleaning, features, models) in `src/` as `.py` files and import it.
- Always `git pull` before you start and `git push` when you finish.
- If you add a package, update `requirements.txt` and mention it in your commit.