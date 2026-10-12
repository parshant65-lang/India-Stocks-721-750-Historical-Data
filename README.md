# India-Stocks-721-750-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 721 to 750)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-721-750-Historical-Data/
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

## 📦 Constituents (721 to 750)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 721 | `AXTEL` | Axtel Industries Limited | `AXTEL.NS` |
| 722 | `AYE` | Aye Finance Limited | `AYE.NS` |
| 723 | `AYMSYNTEX` | AYM Syntex Limited | `AYMSYNTEX.NS` |
| 724 | `AZADIND` | Azad India Mobility Limited | `AZADIND.NS` |
| 725 | `BAFNAPH` | Bafna Pharmaceuticals Limited | `BAFNAPH.NS` |
| 726 | `BAGFILMS` | B.A.G Films and Media Limited | `BAGFILMS.NS` |
| 727 | `BAIDFIN` | Baid Finserv Limited | `BAIDFIN.NS` |
| 728 | `BAJAJCON` | Bajaj Consumer Care Limited | `BAJAJCON.NS` |
| 729 | `BAJAJELEC` | Bajaj Electricals Limited | `BAJAJELEC.NS` |
| 730 | `BAJAJHCARE` | Bajaj Healthcare Limited | `BAJAJHCARE.NS` |
| 731 | `BAJAJHIND` | Bajaj Hindusthan Sugar Limited | `BAJAJHIND.NS` |
| 732 | `BAJAJINDEF` | Indef Manufacturing Limited | `BAJAJINDEF.NS` |
| 733 | `BAJAJST` | Bajaj Steel Industries Limited | `BAJAJST.NS` |
| 734 | `BAJEL` | Bajel Projects Limited | `BAJEL.NS` |
| 735 | `BALAJEE` | Shree Tirupati Balajee Agro Trading Company Limited | `BALAJEE.NS` |
| 736 | `BALAJITELE` | Balaji Telefilms Limited | `BALAJITELE.NS` |
| 737 | `BALAMINES` | Balaji Amines Limited | `BALAMINES.NS` |
| 738 | `BALAXI` | BALAXI PHARMACEUTICALS LIMITED | `BALAXI.NS` |
| 739 | `BALKRISHNA` | Balkrishna Paper Mills Limited | `BALKRISHNA.NS` |
| 740 | `BALMLAWRIE` | Balmer Lawrie & Company Limited | `BALMLAWRIE.NS` |
| 741 | `BALPHARMA` | Bal Pharma Limited | `BALPHARMA.NS` |
| 742 | `BALUFORGE` | Balu Forge Industries Limited | `BALUFORGE.NS` |
| 743 | `BANARBEADS` | Banaras Beads Limited | `BANARBEADS.NS` |
| 744 | `BANARISUG` | Bannari Amman Sugars Limited | `BANARISUG.NS` |
| 745 | `BANCOINDIA` | Banco Products (I) Limited | `BANCOINDIA.NS` |
| 746 | `BANG` | Bang Overseas Limited | `BANG.NS` |
| 747 | `BANKA` | Banka BioLoo Limited | `BANKA.NS` |
| 748 | `BANSALWIRE` | Bansal Wire Industries Limited | `BANSALWIRE.NS` |
| 749 | `BANSWRAS` | Banswara Syntex Limited | `BANSWRAS.NS` |
| 750 | `BASF` | BASF India Limited | `BASF.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream AXTEL 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-721-750-Historical-Data/main/AXTEL/1m/2026/10/AXTEL_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
