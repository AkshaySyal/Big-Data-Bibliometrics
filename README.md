# Publication-Big-Data-Analysis
This project involved extracting and analyzing bibliometric data from an Aminer dataset using MongoDB aggregation pipelines to compute statistics, investigate data accuracy issues and characterize distributions and trends.

# Problem Statement
![image](https://github.com/user-attachments/assets/199d59bf-f0a6-4967-83c3-1e9b3ef7ac38)

# Solution Summary
- Conducted a **comprehensive bibliometric analysis** on the Aminer dataset.

- **Data Preprocessing**:
  - Extracted publication details (IDs, authors, venues, years, citations) from `acm.txt`.
  - Stored extracted data in JSON format.
  - Total records processed: **2,385,067 publications**.

- **Database Analysis**:
  - Used **MongoDB aggregation pipelines** for metric analysis.
  - Computed:
    - Distinct authors: **1,651,650**
    - Distinct venues: **273,330** (noted inaccuracies due to inconsistent naming, e.g., same conference with different yearly names)
    - Publications: **2,385,058**
    - Citations: **1,007,495**

- **Key Insights**:
  - Highly **skewed distributions**:
    - Publications per author and per venue show means much higher than medians.
    - Indicates dominance by a few prolific authors/venues.
  - Top venue by publications: **IEEE Transactions on Information Theory** (12,754 publications).
  - Histograms for references and citations showed high but plausible counts reflecting scientific impact diversity.

- **Venue Impact Factor Analysis**:
  - Initial top value (AI EDAM at 82,080.0) seemed implausible.
  - Recalculated using only venues with ≥10 publications yielded more credible impact factor distributions.
  - Still observed notable **mean-median gaps** in citation counts.

- **Trend Analysis Over Time**:
  - **Average references per publication**: generally increasing.
  - **Average citations per publication**: stagnant for years, with a recent upward trend.

- **Conclusion**:
  - Analysis highlighted data cleaning challenges (e.g., venue naming).
  - Identified structural patterns and evolving trends in scientific publishing.
