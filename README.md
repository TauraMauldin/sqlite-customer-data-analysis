# 1. Clone
git clone https://github.com/<your-org>/sqlite-customer-data-analysis.git
cd sqlite-customer-data-analysis

# 2. Create environment
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt      # sqlite-utils, pandas, seaborn, jupyter, tqdm …

# 3. Build the SQLite DB (optional — pre-built file already committed)
make build-db                        # or: python src/build_db.py

# 4. Explore in the CLI
sqlite-utils tables data/sqlite_customer_db.sqlite
sqlite3 data/sqlite_customer_db.sqlite ".schema customers"

# 5. Run analysis in Jupyter
jupyter lab
# open notebooks/01_exploratory.ipynb
