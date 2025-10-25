# App-Traffic-IVT-Analysis-Report
📌 Final Results from IVT Traffic Analysis
🧮 Total Weeks Analyzed
- The dataset spans multiple weeks of app traffic data.
- Cleaned and processed the data to ensure accuracy.
🚨 IVT Detection Summary
Applied three rules to flag invalid traffic:
- IDFA-UA Ratio > 5.0
- Requests per IDFA > 200
- Zero Impressions per IDFA
Based on these rules:
- IVT Weeks Count: df['computed_ivt'].sum() → This gives the number of weeks flagged as suspicious.
- Normal Weeks Count: len(df) - df['computed_ivt'].sum() → These weeks showed normal traffic behavior.
- IVT Weeks List: A list of dates where IVT was detected.
📈 Visual Insights
- Plotted two key metrics over time:
- requests_per_idfa
- idfa_ua_ratio
- The interactive graph helps spot spikes or unusual trends that may explain IVT flags.
📋 Summary Dictionary Output
summary = {
    'Total Weeks': 94,
    'IVT Weeks Count': np.int64(90),
    'Normal Weeks Count': np.int64(4),
    'IVT Weeks': ['11 Sep to 15 Sep', '2025-09-11 0:00:00', '2025-09-12 0:00:00', '2025-09-13 0:00:00', '2025-09-14 0:00:00', '2025-09-15 0:00:00', '2025-09-11 14:00:00', '2025-09-11 15:00:00', '2025-09-11 16:00:00', '2025-09-11 17:00:00', '2025-09-11 18:00:00', '2025-09-11 19:00:00', '2025-09-11 20:00:00', '2025-09-11 21:00:00', '2025-09-11 22:00:00', '2025-09-11 23:00:00', '2025-09-12 0:00:00', '2025-09-12 1:00:00', '2025-09-12 2:00:00', '2025-09-12 3:00:00', '2025-09-12 4:00:00', '2025-09-12 5:00:00', '2025-09-12 6:00:00', '2025-09-12 7:00:00', '2025-09-12 8:00:00', '2025-09-12 9:00:00', '2025-09-12 10:00:00', '2025-09-12 11:00:00', '2025-09-12 12:00:00', '2025-09-12 13:00:00', '2025-09-12 14:00:00', '2025-09-12 15:00:00', '2025-09-12 16:00:00', '2025-09-12 17:00:00', '2025-09-12 18:00:00', '2025-09-12 19:00:00', '2025-09-12 20:00:00', '2025-09-12 21:00:00', '2025-09-12 22:00:00', '2025-09-12 23:00:00', '2025-09-13 0:00:00', '2025-09-13 1:00:00', '2025-09-13 2:00:00', '2025-09-13 3:00:00', '2025-09-13 4:00:00', '2025-09-13 5:00:00', '2025-09-13 6:00:00', '2025-09-13 7:00:00', '2025-09-13 8:00:00', '2025-09-13 9:00:00', '2025-09-13 10:00:00', '2025-09-13 11:00:00', '2025-09-13 12:00:00', '2025-09-13 13:00:00', '2025-09-13 14:00:00', '2025-09-13 15:00:00', '2025-09-13 16:00:00', '2025-09-13 17:00:00', '2025-09-13 18:00:00', '2025-09-13 19:00:00', '2025-09-13 20:00:00', '2025-09-13 21:00:00', '2025-09-13 22:00:00', '2025-09-13 23:00:00', '2025-09-14 0:00:00', '2025-09-14 1:00:00', '2025-09-14 2:00:00', '2025-09-14 3:00:00', '2025-09-14 4:00:00', '2025-09-14 5:00:00', '2025-09-14 6:00:00', '2025-09-14 7:00:00', '2025-09-14 8:00:00', '2025-09-14 9:00:00', '2025-09-14 10:00:00', '2025-09-14 11:00:00', '2025-09-14 12:00:00', '2025-09-14 13:00:00', '2025-09-14 14:00:00', '2025-09-14 15:00:00', '2025-09-14 16:00:00', '2025-09-14 17:00:00', '2025-09-14 18:00:00', '2025-09-14 19:00:00', '2025-09-14 20:00:00', '2025-09-14 21:00:00', '2025-09-14 22:00:00', '2025-09-14 23:00:00', '2025-09-15 0:00:00', '2025-09-15 1:00:00']
}



🧠 What This Means
- You we know which weeks had suspicious traffic and why they were flagged.
- This helps us investigate which apps or traffic sources might be causing IVT.
- We can now compare IVT vs. non-IVT weeks to improve app performance or ad quality.


