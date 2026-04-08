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
