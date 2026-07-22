# Fuel Price Volatility vs. Two-Wheeler Resale Value

An interactive dashboard exploring whether fuel price spikes lift resale value
for fuel-efficient bikes more than less efficient ones — with a global
comparison against US fuel price trends.

**Data note:** the CSVs here are synthetically generated (`generate_data.py`),
calibrated to real published fuel price anchor points (Delhi/Mumbai/Bengaluru
metro prices, US EIA-style historical trends). This is disclosed inside the
app itself — be upfront about this in interviews, it's a legitimate, honest
way to demonstrate the analysis methodology. Swapping in real Kaggle CSVs
later (same column names) would work without changing the app code.

## Files
- `generate_data.py` — builds the 3 datasets
- `app.py` — the Streamlit dashboard
- `india_fuel_prices.csv`, `us_fuel_prices.csv`, `india_bike_resale.csv` — data
- `requirements.txt` — dependencies for deployment

## Push it live — entirely from your phone, no laptop needed

### Step 1: Put the code on GitHub
1. Go to **github.com** in your phone browser, log in (or sign up free).
2. Tap the **+** icon (top right) → **New repository**.
3. Name it e.g. `fuel-bike-analytics` → make it **Public** → tap **Create repository**.
4. On the new repo page, tap **"uploading an existing file"** (a link in the
   quick-setup box).
5. Upload every file in this project folder: `app.py`, `requirements.txt`,
   `generate_data.py`, and all 3 `.csv` files.
6. Scroll down, tap **Commit changes**.

### Step 2: Deploy on Streamlit Community Cloud (free)
1. Go to **share.streamlit.io** in your phone browser.
2. Tap **Sign in** → choose **Continue with GitHub** → authorize it.
3. Tap **"Create app"** → **"Yup, I have an app"**.
4. Pick your repo (`fuel-bike-analytics`), branch (`main`), and set the main
   file path to **`app.py`**.
5. Tap **Deploy**.
6. Wait 1-3 minutes while it installs dependencies and builds — you'll see a
   live log. When it finishes, you get a public URL like
   `https://your-app-name.streamlit.app` — that's your live link.

### Step 3: Share it
Put that link in your resume, LinkedIn, and portfolio README. Anyone can open
it on their phone or laptop instantly — no install needed on their end either.

## If deployment fails
- Most common cause: a typo in `requirements.txt` or a missing file upload —
  double check all 5 files (app.py + requirements.txt + 3 CSVs) are in the repo root.
- Streamlit Cloud shows the exact error in its build log — screenshot it and
  we can debug from there.

## Talking points for interviews
- "I identified a non-obvious question — whether fuel price volatility
  differentially affects resale value based on a vehicle's fuel efficiency."
- "I controlled for confounders (bike age, model) using a residual-based
  approach rather than relying on a raw, misleading correlation."
- "I built and deployed a live interactive dashboard, not just a static notebook."
