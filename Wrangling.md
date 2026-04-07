# ICT Exports Wrangling 

Metric Specificity: Identified that the dataset measures ICT goods exports as a percentage of total goods exports.

Target Filtering: Filtered for the top 5 global economies plus Canada using ISO3 codes (USA, CHN, DEU, JPN, IND, CAN).

Timeline Constraint: Removed data prior to 2010 to focus the analysis on the post-smartphone/modern AI era.The 'Year' column represents the most recent verified annual reporting from the World Bank. While the project decision is set in 2026, 2022/2024 data serves as the baseline for forecasting future trends

Column Reduction: Trimmed 43 metadata columns down to 4 essential columns (Country, Code, Year, Value) to improve data readability for the CMO.

Handling Nulls: Confirmed that the target economies have consistent reporting for this indicator across the selected timeline, requiring no imputation.

# Mobile Broadband Data Wrangling

Filter Logic: Filtered the TYPE_LABEL column to include only "Type: Value". Excluded "Rank" and "Score" as they are relative metrics and don't represent the raw infrastructure growth needed for AI personalization analysis.

Target Selection: Filtered REF_AREA for CAN, USA, CHN, DEU, JPN, and IND to focus on the top global economies relevant to a mid-sized firm's expansion.

Reshaping: Pivoted the year columns (2019, 2021, 2024) into a single "Year" column (Long Format) to allow for easier trend-line plotting in Excel.

Data Note: Observed that Japan and the USA have significantly higher mobile penetration (over 100 per 100 people, indicating multiple devices per person), which suggests a highly saturated market for AI targeting.

# Regulatory Quality Data Wrangling 

Choice of Metric: Switched from raw "Estimate" scores to "Percentile Rank" to provide the CMO with a more relative, comparative metric of global regulatory standing.

Filtering Target Markets: Used the REF_AREA column to isolate the six key economies (USA, CHN, DEU, JPN, IND, CAN) to allow for a direct competitive landscape analysis.

Timeline Standardization: Filtered for 2010–2023 to maintain synchronization with your previous technical infrastructure datasets (Internet, Mobile, ICT).

Data Formatting: Removed 39 auxiliary metadata columns (like STRUCTURE_ID and UNIT_MULT) to keep the data clean and accessible in a simple CSV format.

# Secure Servers Data Wrangling 

Variable Context: Identified WB_WDI_IT_NET_SECR_P6 as the primary indicator for transactional infrastructure capacity.

Target Isolation: Filtered the dataset for the specific 6 global markets (CAN, USA, CHN, DEU, JPN, IND) to allow the CMO to compare infrastructure readiness across expansion zones.

Temporal Filtering: Constrained the dataset to 2010–2024. This specific window captures the transition from "Traditional E-commerce" to "AI-Driven Personalization," marked by the massive spike in server density starting around 2016.

Data Scale Adjustment: Noted the massive variance in scale (from single digits in 2010 to hundreds of thousands in 2024). Using a Logarithmic Scale for visualizations to ensure smaller growth trends in emerging markets (like India) remain visible.

# Individual Internet User Data Wrangling 

Variable Selection: Isolated WB_WDI_IT_NET_USER_ZS, which measures the percentage of the population that has used the internet from any device in the last 3 months.

Geographic Focus: Filtered for the project’s 6 target markets (CAN, USA, CHN, DEU, JPN, IND) using the REF_AREA standard codes.

Time Normalization: Filtered all observations to the 2010–2024 window to ensure perfect synchronization with the "Secure Servers" and "Mobile Broadband" datasets for multi-variable analysis.

Data Cleaning: Removed 39 columns of non-essential metadata. Confirmed that World Bank "percentage" values were consistently stored as floats (e.g., 94.4 for 94.4%) to avoid calculation errors in Excel/Tableau.
