# Option Pricing Models — Black–Scholes, Binomial Tree, Monte Carlo (Streamlit App)

Interactive **Streamlit** web app to price European options using:
1) **Black–Scholes**, 2) **Monte Carlo**, 3) **Binomial Tree**.

Fetches price data, lets you set parameters, and visualizes outcomes.

---

## 🔧 Features

- European call/put pricing with **Black–Scholes**
- **Monte Carlo** path simulation and payoff estimation
- **Binomial Tree** (CRR) valuation
- Parameter inputs: Strike, Risk-free rate, Volatility (σ), Exercise date
- Data fetch with `pandas-datareader` / caching via `requests-cache`
- Streamlit UI with quick scenario testing

---

## 📂 Structure

- `option_pricing/` — Model implementations (BSM / MC / Binomial)
- `streamlit_app.py` — Main web app
- `demo/` — GIFs of the app
- `Requirements.txt` — Python deps
- `Dockerfile` — Containerized run

---

## 🚀 Run Locally

```bash
python -m venv .venv
source .venv/bin/activate    # (Windows) .venv\Scripts\activate
pip install -r Requirements.txt
streamlit run streamlit_app.py --server.port 8080
# open http://localhost:8080
🐳 Run with Docker
bash
Copy code
docker build -t options-pricing:latest .
docker run -p 8080:8080 options-pricing:latest
# open http://0.0.0.0:8080
# option-pricing-streamlit-bsm-binomial-montecarlo
