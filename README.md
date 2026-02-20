# 📊 Credit Risk Portfolio Analysis  
### Excel (Data Preparation & Pivot Analysis) + Power BI (Interactive Dashboard)


# 🏦 Executive Summary

This analysis evaluates a 1,200-customer credit Analysis that answers how credit risk is distributed across branches and employment types.  

Using Excel for data preparation and pivot-based aggregation [Link](https://github.com/Edwin-Debrah/Credit-Risk-Analysis---Excel/blob/main/Credit_Risk_Analysis.xlsm), followed by Power BI for interactive visualization [Link](https://github.com/Edwin-Debrah/Credit-Risk-Analysis---Excel/blob/main/Credit%20Risk%20Analysis.pbix), the analysis uncovers structural risk patterns, segmentation imbalances, and operational inefficiencies in classification logic.

At portfolio level, the numbers immediately tell a story:

- 75.33% of customers fall into the **Medium Risk (Review)** category  
- 20.08% are classified as **Low Risk (Approve)**  
- Only 2.67% are labeled **High Risk (Reject)**  
- Average Debt-to-Income (DTI) ratio stands at **0.44**  
- Average Days Past Due is **37.86 days**

<img width="1130" height="619" alt="Screenshot 2026-02-20 131917" src="https://github.com/user-attachments/assets/6455840a-b0ff-4ec3-bfae-fc1572cde2cd" />


The concentration in Medium Risk suggests a cautious underwriting framework, but it also raises questions about segmentation sharpness and review workload efficiency.

This analysis investigates where risk truly lives inside the portfolio.


# 🎯 Business Context

In lending environments, risk type must balance growth with protection. Too many high-risk approvals increase defaults. Too many manual reviews slow down decision-making and reduce scalability.

This analysis answers three critical strategic questions:

1. Are some branches carrying disproportionate risk exposure?
2. Which employment types are financially overstretched?
3. Does the current risk classification align with financial stress indicators like DTI and delinquency?


# 🏬 Branch-Level Risk Story

Across the five branches — Accra Central, Kumasi Main, Takoradi, Tamale, and Tema — customer distribution appears relatively balanced. However, financial stress indicators reveal meaningful differences.

Tamale (258 customers) and Takoradi (257 customers) carry the largest exposure volumes, with over 190 customers each classified as Medium Risk. This creates significant operational review concentration in those locations.

Accra Central records the highest number of High-Risk customers (13), paired with an average DTI of 0.38 and 39.22 average days past due. While its DTI is not the highest, its elevated rejection count suggests stronger risk flagging behavior.

The most striking anomaly appears in Kumasi Main:

- Average DTI: **0.82 (highest in the portfolio)**
- Average Days Past Due: **40.66 (highest among branches)**

<img width="1135" height="630" alt="Screenshot 2026-02-20 131945" src="https://github.com/user-attachments/assets/2360beaa-7635-4836-a6d8-17bba61d00dc" />


Despite these financial stress signals, Kumasi does not lead in High-Risk classification. This suggests most of their borrowers have either a medium score after the combination of all 3 factors (Stability + DTI + Deliquency) compared to Accra which requires review.

In contrast, Tema appears structurally healthier:

- Lowest High-Risk count (3 customers)
- Lowest Average DTI (0.30)
- Lower delinquency levels (35.70 days)

From a portfolio growth standpoint, Tema represents the most stable expansion candidate.


# 👔 Employment-Based Risk Narrative

When examining employment segmentation, deeper structural risk patterns emerge.

Salaried customers demonstrate the strongest financial stability:

- Average DTI: 0.318  
- Average Days Past Due: 36.05  
- 30.46% classified as Low Risk  
- 0% classified as High Risk

<img width="1133" height="630" alt="Screenshot 2026-02-20 132012" src="https://github.com/user-attachments/assets/0d8661c2-bf2e-436b-9bbc-a7aa1a9f57af" />


This segment shows predictable income stability and consistent repayment behavior, making it the safest portfolio backbone.

The Self-Employed segment tells a different story.

- Average DTI: 0.63  
- Average Days Past Due: 40.03  
- 68.57% in Medium Risk  
- 0% officially High Risk  

Despite having the highest leverage ratio and highest delinquency average, this segment is not proportionally flagged as high risk, but have the third highest medium risk which needs a critical review before proceeding. This indicates a potential structural bias or overly tolerant classification threshold.

Unemployed customers exhibit the highest explicit rejection rate:

- 9.41% High Risk  
- 88.61% Medium Risk  
- 0% Low Risk approvals  

Here, underwriting appears appropriately conservative.

Contract workers sit between stability and vulnerability. While their DTI remains moderate (0.33), delinquency averages are elevated (38.41 days), and 6.28% are classified as High Risk. Income volatility may be influencing repayment behavior.


# 🔍 Structural Risk Observations

Three overarching patterns emerge from the analysis:

### 1️⃣ Medium Risk Dominance

With 75.33% of the portfolio sitting in Medium Risk, the segmentation logic appears compressed. This creates operational bottlenecks and may indicate thresholds that are too conservative or not sufficiently differentiated.

### 2️⃣ DTI and Classification Misalignment

In both Kumasi Main and the Self-Employed segment, DTI levels are significantly elevated, yet High-Risk classification remains low.

This suggests that:

- DTI thresholds may not be strongly weighted in risk scoring.
- Risk classification logic may rely on additional unobserved factors.
- There may be room for recalibration.

### 3️⃣ DTI as a Strong Risk Signal

Segments with higher DTI consistently show higher average Days Past Due. The relationship confirms DTI as a meaningful indicator of repayment stress.


# 💡 Strategic Recommendations

Based on the findings, several actions are advisable:

### Recalibrate Risk Thresholds

Introduce stronger DTI-based classification triggers, especially for segments exceeding 0.60 leverage. This would sharpen differentiation between Medium and High Risk.

### Strengthen Monitoring of Self-Employed Borrowers

Given their elevated leverage and delinquency levels, additional documentation or income stability validation should be considered during underwriting.

### Reduce Medium Risk Concentration

Refine segmentation logic to reduce the 75% review burden. Clearer separation between Low and High Risk will improve operational efficiency.

### Target Growth in Stable Segments

Expand lending efforts in:
- Salaried customers
- Tema branch

These segments demonstrate lower structural stress.


# ⚠ Assumptions

This analysis assumes:

- DTI is calculated as total debt divided by income.
- Risk categories were pre-assigned based on internal scoring logic, that is, Stability + Deliquency + DTI ratio.
- The dataset represents a static snapshot (no time dimension included).
- External macroeconomic factors are not integrated.


# 🚧 Caveats

- No predictive modeling was applied.
- No credit score variable was available.
- Income volatility trends were not tracked.
- Results reflect descriptive, not predictive, analytics.


# 🛠 Technical Implementation

Data preparation and segmentation logic were developed in Excel using pivot tables and aggregation modeling.

The dashboard layer in Power BI includes:

- DAX-based KPI measures  
- Cross-filtered segmentation visuals  
- Branch and employment drill-down  
- Risk distribution summaries  

The full workflow demonstrates an end-to-end analytical pipeline: from raw data structuring to decision-ready storytelling.


# 📈 Final Conclusion

The portfolio is not immediately distressed, but it shows structural segmentation inefficiencies.

Risk exposure is concentrated in:

- Contract and unemployed borrowers  
- Accra Central and Kumasi Main branches  
- High-DTI segments  

While outright High-Risk classifications remain low, financial stress indicators suggest recalibration is warranted.

This analysis demonstrates portfolio thinking, risk interpretation, and the ability to translate data into actionable financial strategy.
