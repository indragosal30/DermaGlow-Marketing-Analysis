# DermaGlow Marketing Analysis

## Background
Project analisis marketing brand skincare fiktif DermaGlow yang mencakup 
tiga scope analisis menggunakan Meta Ads dataset:

1. **A/B Testing Analysis** — Membandingkan performa dua creative variant: 
   Video_Review vs Static_Catalog dari sisi CTR, CVR, CPC, dan ROAS
2. **Funnel Analysis** — Mengidentifikasi stage drop-off terbesar dan 
   mengukur business impact dari kebocoran funnel
3. **Campaign Analysis** *(Coming Soon)*

## Tools
- **Python** (pandas, numpy, scipy) — Data Cleaning & Analysis
- **Jupyter Notebook** — Development Environment
- **Power BI** — Data Visualization & Dashboard
- **GitHub** — Version Control & Portfolio Documentation

## Dataset
- `marketing_ads_data.csv` — 1.000 baris data Meta Ads (setelah cleaning)
- `sales_transaction_data.csv` — 2.495 baris data transaksi (setelah cleaning)
- `ad_summary_clean.csv` — Gabungan agregasi marketing ads & sales transaction

## Methodology
Analisis menggunakan framework **OSEMN**:
1. **Obtain** — Load data marketing ads dan sales transaction
2. **Scrub** — Handling missing values, duplikat, format date, outlier
3. **Explore** — Kalkulasi metrik (CTR, CVR, CPC, ROAS), funnel & segment analysis
4. **Model** — Shapiro-Wilk Test & Mann-Whitney U Test untuk statistical significance
5. **Narrate** — Business insights & actionable recommendations

## Key Findings

### A/B Testing Analysis
- **Static_Catalog** unggul di ROAS (3.40 vs 1.77) dan Total Revenue (Rp332M vs Rp196M)
- **Video_Review** unggul di CTR (0.0250 vs 0.0119) dan CPC (Rp1.117 vs Rp2.538)
- Perbedaan signifikan secara statistik di semua metrik (Mann-Whitney U, p < 0.05)
- Kombinasi terkuat: **Static_Catalog + Warm Audience + Sunscreen** (ROAS 4.35)

### Funnel Analysis
- Drop-off kritis terjadi di stage **Add to Cart → Transactions**, bukan di stage lain
- Static_Catalog konsisten unggul di cart conversion rate di semua segment (~4x Video_Review)
- Video_Review efektif top funnel (CTR 2x lebih tinggi) namun bocor di bottom funnel
- **Sunscreen** adalah hero product — top performer di kedua variant
- 1.945 transaksi Video_Review tidak terealisasi = **Rp552 juta revenue hilang**

## Recommendation
Hybrid strategy — kedua variant dijalankan bersamaan dalam funnel terintegrasi:
- **Video_Review** → Top Funnel, cold audience, awareness & traffic acquisition
- **Static_Catalog** → Bottom Funnel, warm audience, konversi & revenue
- Prioritas perbaikan: Fix cart conversion Video_Review (potensi Rp552 juta)
- Prioritas scale: Static_Catalog + Warm Audience + Sunscreen (ROAS 4.35)

## Dashboard Preview
![A/B Testing - Overall Performance](dashboard/overall_performance.png)
![A/B Testing - Segment Analysis](dashboard/segment_analysis.png)
![Funnel Analysis](dashboard/funnel_analysis.png)
![Business Recommendation](dashboard/business_recommendation.png)
