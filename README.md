# PowerBid

AI-powered bidding assistant for the Turkish day-ahead electricity market (GÖP).

## What it does

PowerBid combines three data sources to recommend optimal bid prices:

1. **Historical PTF patterns** — hourly price statistics from EPİAŞ (2025-2026)
2. **Weather forecast** — temperature, solar radiation, wind speed via Open-Meteo API
3. **System conditions** — generation vs demand balance via EPİAŞ Transparency Platform

**Output:** For each hour of the next day:
- Predicted PTF range
- Recommended bid price
- Acceptance probability (%)
- Risk score

## Architecture
Data Layer    → EPİAŞ API + Open-Meteo API + System status
Model Layer   → Pattern model + Weather model + Anomaly detection
Decision Layer → PTF forecast + Bid suggestion + Risk score
Output        → Daily bid report
## Tech Stack

Python, pandas, scikit-learn, EPİAŞ eptr2, Open-Meteo API

## Status

- [x] Historical PTF analysis (8,784 hours)
- [x] GÖP-GİP spread analysis
- [x] Hourly bid confidence intervals
- [ ] Weather model integration
- [ ] PTF forecasting model
- [ ] Automated bid report

## Data Sources

- [EPİAŞ Şeffaflık Platformu](https://seffaflik.epias.com.tr)
- [Open-Meteo](https://open-meteo.com)
