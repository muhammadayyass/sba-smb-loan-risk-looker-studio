# SBA Small-Business Loan Risk Dashboard — Looker Studio

Analyzing which small-business segments carry the highest loan-default risk, using official U.S. government loan-guarantee data.

![Dashboard Overview](screenshots/dashboard-overview.png)

🔗 **[Open Live Dashboard](https://datastudio.google.com/reporting/ae835611-422a-4b42-816d-1a73065ab196)**

## Business Problem
Government-backed small-business loan programs (like the U.S. SBA 7(a) — structurally similar to Indonesia's KUR scheme) need to understand which sectors and lenders carry disproportionate default risk, so guarantee capacity and risk oversight can be allocated accordingly.

## Data
- **Source:** Official U.S. Small Business Administration data (data.sba.gov), FY2020–Present
- **Scope:** Filtered to Food & Beverage (NAICS 72) and Retail (NAICS 44-45) sectors, chosen deliberately for relevance to prior QRIS/UMKM payment-ecosystem work at Bank Indonesia
- **Resolution filter:** Only loans with a final outcome — Paid in Full (PIF) or Charged Off (CHGOFF) — 2,987 loans. Still-active loans were excluded so the default-rate metric isn't biased by loans that haven't had time to succeed or fail yet.

## Tools & Techniques
Looker Studio · data cleaning (corrected a mis-scaled tenor field found during validation) · geographic and sector-level aggregation with small-sample filtering

## Key Findings
- **~$12.98B** total disbursed across 2,987 resolved loans
- Overall **NPL (default) rate: 13.46%** — above healthy commercial-bank benchmarks (~5%), though SMB lending carries structurally higher risk than corporate lending globally
- Average tenor: 128 months (~10.6 years); average 23.9 days from approval to disbursement
- **The Huntington National Bank** is the largest lender by volume ($778M), well ahead of #2 Celtic Bank Corporation ($466M)
- **Electronic Shopping** is the riskiest sub-sector (45.16% NPL), followed by Cosmetics & Beauty Supplies (36.59%) — high-value, trend-sensitive retail categories carry more risk than essential F&B categories like Caterers (21.43%, lowest in the dataset)
- State-level risk maps are deliberately limited to states with ≥10 loans to avoid small-sample distortion

## Recommendation
Tighten credit scoring for high-value, trend-sensitive retail sub-sectors. Monitor higher-NPL states (Hawaii, New York among sufficiently-sampled states) for regional policy review. Consider risk-management training partnerships with high-volume lenders given their concentrated exposure.

## Limitations
Analysis is restricted to loans with a final outcome (PIF/CHGOFF), so more recently originated loans are under-represented — this is a snapshot of historically resolved risk, not a real-time predictor. Findings are U.S.-specific; applying the same *methodology* to Indonesian KUR/UMKM credit data would require access to equivalent loan-level records.

---
**Author:** Muhammad Yahya Ayyasy — [LinkedIn](https://linkedin.com/in/muhammadayyass) · muhammadayyas22@gmail.com
