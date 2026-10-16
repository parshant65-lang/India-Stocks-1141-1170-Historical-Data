# India-Stocks-1141-1170-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 1141 to 1170)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-1141-1170-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (1141 to 1170)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 1141 | `GICL` | Globe International Carriers Limited | `GICL.NS` |
| 1142 | `GILLANDERS` | Gillanders Arbuthnot & Company Limited | `GILLANDERS.NS` |
| 1143 | `GINNIFILA` | Ginni Filaments Limited | `GINNIFILA.NS` |
| 1144 | `GIPCL` | Gujarat Industries Power Company Limited | `GIPCL.NS` |
| 1145 | `GKB` | GKB Ophthalmics Limited | `GKB.NS` |
| 1146 | `GKENERGY` | GK Energy Limited | `GKENERGY.NS` |
| 1147 | `GKSL` | Gujarat Kidney And Super Speciality Limited | `GKSL.NS` |
| 1148 | `GKWLIMITED` | GKW Limited | `GKWLIMITED.NS` |
| 1149 | `GLASSWALL` | Glass Wall Systems (India) Limited | `GLASSWALL.NS` |
| 1150 | `GLFL` | Gujarat Lease Financing Limited | `GLFL.NS` |
| 1151 | `GLOBAL` | Global Education Limited | `GLOBAL.NS` |
| 1152 | `GLOBALE` | Globale Tessile Limited | `GLOBALE.NS` |
| 1153 | `GLOBALVECT` | Global Vectra Helicorp Limited | `GLOBALVECT.NS` |
| 1154 | `GLOBE` | GLOBE ENTERPRISES (INDIA) LIMITED | `GLOBE.NS` |
| 1155 | `GLOBECIVIL` | Globe Civil Projects Limited | `GLOBECIVIL.NS` |
| 1156 | `GLOBUSSPR` | Globus Spirits Limited | `GLOBUSSPR.NS` |
| 1157 | `GLOSTERLTD` | Gloster Limited | `GLOSTERLTD.NS` |
| 1158 | `GLOTTIS` | Glottis Limited | `GLOTTIS.NS` |
| 1159 | `GMBREW` | GM Breweries Limited | `GMBREW.NS` |
| 1160 | `GMMPFAUDLR` | GMM Pfaudler Limited | `GMMPFAUDLR.NS` |
| 1161 | `GMRP&UI` | GMR Power and Urban Infra Limited | `GMRP&UI.NS` |
| 1162 | `GNA` | GNA Axles Limited | `GNA.NS` |
| 1163 | `GNFC` | Gujarat Narmada Valley Fertilizers and Chemicals Limited | `GNFC.NS` |
| 1164 | `GNRL` | Gujarat Natural Resources Limited | `GNRL.NS` |
| 1165 | `GOACARBON` | Goa Carbon Limited | `GOACARBON.NS` |
| 1166 | `GOCLCORP` | GOCL Corporation Limited | `GOCLCORP.NS` |
| 1167 | `GOCOLORS` | Go Fashion (India) Limited | `GOCOLORS.NS` |
| 1168 | `GODAVARIB` | Godavari Biorefineries Limited | `GODAVARIB.NS` |
| 1169 | `GODIGIT` | Go Digit General Insurance Limited | `GODIGIT.NS` |
| 1170 | `GODREJAGRO` | Godrej Agrovet Limited | `GODREJAGRO.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream GICL 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-1141-1170-Historical-Data/main/GICL/1m/2026/10/GICL_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
