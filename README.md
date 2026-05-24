# TripSky Sales Analysis and Marketing Recommendations

Academic data analysis project for TripSky, a French niche travel company (adventure, relaxation, culture). The goal is to identify which destination x season x trip type segments to prioritize and whether ad spend is underperforming.

## Repository contents

- [TripSky_Analyse.ipynb](TripSky_Analyse.ipynb) - Notebook with EDA, cleaning, visualizations, insights, and recommendations.
- [company.csv](company.csv) - Daily company metrics (date, customers, sales revenue, ad spend, bookings).
- [cutomers.csv](cutomers.csv) - Customer trip data (demographics, trip type, destination, season, duration, party size, total price, payment, rating, trip dates, annual budget).
- [TripSky-Analysis.pptx](TripSky-Analysis.pptx) - Presentation slides.
- [TripSky_Rapport.docx](TripSky_Rapport.docx) - Written report.

## Data notes

- Two CSVs of roughly ~800 rows each (daily activity and customer trips).
- The notebook flags data quality issues: duplicate rows, outlier ages (350, 220, 4100), missing values (destination, trip type, gender, payment, dates), and inconsistent casing in categorical fields.
- Column names are in French in the source files.

## Key findings (from the notebook)

- Revenue concentrates in a small set of destinations, led by Japan, Bali, and Norway.
- Strong seasonality: summer and winter dominate; spring is the weakest season.
- Ad spend and daily revenue show near-zero correlation (r ~ 0).
- The core revenue segment is ages 26-45.
- Average rating is about 2.5/5, indicating a quality and retention risk.

## Recommendations

- Reallocate ad spend: cut about 30% from the top 20% highest-spend days and reinvest in CRM/quality.
- Focus marketing on the top 3 destinations x top 2 seasons to lift conversion.
- Prioritize service quality improvements to raise ratings and repeat bookings.

## Run locally

1. Install dependencies:

```bash
pip install pandas numpy matplotlib seaborn
```

2. Open [TripSky_Analyse.ipynb](TripSky_Analyse.ipynb) and update the first cell paths.
	The notebook currently searches in an `../attached_assets` folder using glob patterns.
	Point it to the CSVs in the repo root instead.
3. Run all cells.
