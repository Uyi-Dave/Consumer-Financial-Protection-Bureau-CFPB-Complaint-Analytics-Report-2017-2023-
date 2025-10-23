# Consumer Financial Protection Bureau (CFPB) Complaint Analytics Report (2017-2023)

[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow?logo=powerbi)](https://github.com/Uyi-Dave/Consumer-Financial-Protection-Bureau-CFPB-Complaint-Analytics-Report-2017-2023-/blob/main/Consumer%20Financial%20Complaints%20Analytics.pbix)
[![Dataset](https://img.shields.io/badge/Dataset-CFPB-blue)](https://github.com/Uyi-Dave/Consumer-Financial-Protection-Bureau-CFPB-Complaint-Analytics-Report-2017-2023-/blob/main/Consumer%20Financial%20Complaints%20Dataset.xlsx)

---

## 📋 Table of Contents
1. [Project Background](#project-background)
2. [Executive Summary](#executive-summary)
3. [Dashboards](#dashboards)
4. [Insights Deep-Dive](#insights-deep-dive)
5. [Recommendations](#recommendations)
6. [Caveats and Assumptions](#caveats-and-assumptions)
7. [Technical Implementation](#technical-implementation)

---

## Project Background

As a Data Analyst at the Consumer Financial Protection Bureau (CFPB), I've conducted a comprehensive analysis of consumer financial complaints submitted between May 2017 and August 2023. This report delivers critical insights to key stakeholders including the CFPB's Supervision and Enforcement Division, Policy Team, and Consumer Education Office.

### Key Performance Indicators (KPIs) analyzed include:
- Total complaint volume and growth trends
- Company response timeliness (measured in days)
- Response quality (monetary relief vs. non-monetary resolution)
- Geographic complaint concentration
- Product and issue category performance

These insights will be used by the **Enforcement Division** to prioritize regulatory examinations, the **Policy Team** to strengthen consumer protection regulations, and the **Communications Office** to develop targeted consumer education campaigns. The **Supervision Division** will leverage company-level performance metrics to allocate examination resources more effectively across financial institutions.

### Project Goals
The primary objective is to identify systemic vulnerabilities in the consumer financial services sector by analyzing complaint patterns, company response effectiveness, and emerging risk areas. This analysis aims to answer critical regulatory questions: Which financial products pose the greatest consumer risk? Which companies demonstrate poor complaint resolution practices? Where should the CFPB focus its enforcement and examination resources to maximize consumer protection?

### Data Structure Overview
The dataset contains **62,520 consumer complaints** spanning **1,081 unique financial companies** across all 50 U.S. states and territories. Each record includes complaint metadata (submission date, channel, geographic location), product classification (9 major categories, 60+ sub-products), issue taxonomy (100+ issue and sub-issue combinations), company identifiers, and response outcomes. The data was enriched with company attributes including market share percentages, size tier classifications (Small/Medium/Large), enforcement history flags, and reputation scores (0-100 scale). Response timeliness is measured in calendar days from complaint receipt to company action.

---

## Executive Summary

Between 2017 and 2023, the CFPB received over 62,500 complaints with an impressive **93.77% timely response rate** from financial institutions. However, beneath this positive metric lie significant concerns:

### Critical Findings:
- **Complaint volume surged 135%** from 2017 to a peak in 2023, with the most dramatic spike occurring post-2020, reaching 1,749 monthly complaints before a sharp recent decline to 717 (suggesting potential data lag or regulatory intervention)
- **Checking and savings accounts dominate complaints at 40%** (24,800 complaints), nearly 2x higher than credit cards (16,200)
- **COMP-0342 leads all companies** with 83 complaints despite only 0.10% market share, indicating severe per-capita complaint rates of 8,080 complaints per 1% market share
- **"Managing an account" is the #1 issue** reported (15,100 complaints), followed by incorrect information (4,900) and purchase problems (4,400)
- **Web referral channels receive the fastest responses**, while traditional channels lag significantly
- **Only 23.51% of complaints resulted in monetary relief** for consumers, with 65.65% closed with explanations but no compensation

> **Geographic Alert:** California shows as a high-concentration complaint state, requiring deeper investigation into whether this reflects population size or disproportionate financial services issues.

---

## Dashboards

### Dashboard 1: Complaint Overview & Key Metrics
![Dashboard 1](./Dashboards/Overview%20and%20Key%20Insights%20Dashboard%20(1).png)
*Overview of total complaints, timely response rates, and geographic distribution of complaints across the United States.*

### Dashboard 2: Drivers of Consumer Complaints
![Dashboard 2](./Dashboards/Product,%20Issue%20Analysis%20Dashboard%20(2).png)
*Deep dive into product categories, issues, sub-issues, and submission channels that drive consumer complaints.*

### Dashboard 3: Corporate Response Insights
![Dashboard 3](./Dashboards/Company%20Performance%20Dashboard%20(3).png)
*Analysis of company performance, response times, market share correlations, and enforcement history impact.*

---

## Insights Deep-Dive

### 1. Temporal Trends: The Post-2020 Complaint Explosion

The complaint trajectory tells a concerning story. Starting at 744 monthly complaints in mid-2017, volumes remained relatively stable (600-900 range) through 2020. Beginning in 2021, complaints escalated dramatically, reaching peaks of 1,281 (late 2022) and ultimately 1,749 (early 2023). This 135% increase from baseline suggests either deteriorating service quality, increased consumer awareness of CFPB channels, or systemic disruptions in the financial services sector during the post-pandemic period.

The recent sharp drop to 717 complaints warrants investigation—this could indicate incomplete data for recent months, seasonal variation, or the impact of recent regulatory enforcement actions.

### 2. Geographic Distribution: State-Level Hotspots

The geographic heat map reveals California as a dark red hotspot, followed by moderate-to-high activity in Texas, Florida, and the Northeast corridor. This pattern partially correlates with population density but may also indicate:
- Higher concentrations of financial services activity in these states
- More digitally-engaged populations aware of CFPB complaint channels
- Potential state-level regulatory gaps that leave consumers more vulnerable

States showing lower complaint volumes (Midwest, Mountain West) require investigation—are consumers underserved by awareness campaigns, or do they experience genuinely fewer issues?

### 3. Product Category Analysis: The Checking Account Crisis

**Checking or savings accounts** represent the single largest pain point at 24,800 complaints (39.7% of total volume). Breaking this down by sub-product:
- **Checking accounts alone:** 20,800 complaints (33% of all complaints)
- **General-purpose credit cards:** 13,400 complaints
- **Credit reporting:** 7,300 complaints

This dominance is particularly troubling because checking accounts are foundational financial products—problems here affect consumers' ability to manage daily finances, receive wages, and pay bills. The next tier of products (credit cards at 16,200 and credit reporting at 7,700) are distant seconds, highlighting how basic banking services have become the primary source of consumer frustration.

### 4. Issue & Sub-Issue Breakdown: What's Actually Going Wrong

#### Top-Level Issues:
- **Managing an account:** 15,100 complaints (24% of total)—this broad category suggests fundamental problems with account access, fees, and service quality
- **Incorrect information on credit reports:** 4,900
- **Problems with purchases:** 4,400
- **Account closing issues:** 3,000
- **Payment processing troubles:** 2,800

#### Sub-Issue Specifics Reveal Root Causes:
- **Deposits and withdrawals:** 5,600 complaints—consumers can't access their own money
- **Debit/ATM card problems:** 3,400
- **Credit card company unresponsiveness:** 2,800
- **Information belonging to someone else:** 2,400 (identity-related)
- **Unauthorized account closures:** 2,300

These granular issues point to operational failures: transaction processing errors, poor customer service responsiveness, and inadequate fraud prevention systems that wrongly flag legitimate customers.

### 5. Company Response Analysis: Speed vs. Quality

#### Response Timeliness
The overall 93.77% timely response rate masks important variations:
- **Average response time:** 15.09 days across all companies
- **Large companies respond fastest:** 15.07 days
- **Medium companies:** 15.15 days
- **Small companies lag at 15.45 days** (suggesting resource constraints)

#### Response Quality—The Real Problem:
- **Only 23.51% of complaints resulted in monetary relief**
- **65.65% were closed with explanation only**—companies acknowledged issues but provided no compensation
- **8.43% closed with non-monetary relief**
- **2.39% remain in progress**

This reveals a troubling pattern: companies are meeting regulatory response timeframes but often denying legitimate consumer claims.

#### Enforcement History Correlation
Companies with enforcement histories maintain a 93.7% timely response rate versus 93.9% for those without—virtually identical. This suggests enforcement actions don't meaningfully improve response speed, though response quality data would require deeper analysis.

### 6. Company-Specific Performance: Identifying Bad Actors

#### Highest Raw Complaint Volumes:
- **COMP-0342:** 83 complaints
- **COMP-0276:** 82 complaints
- **COMP-0301:** 82 complaints

However, market share adjustment reveals the real story:

#### Complaints per 1% Market Share (the fairest metric):
- **COMP-0878:** 8,100 complaints per 1% share—the worst performer with 80 complaints and only 0.01% market share
- **COMP-0015:** 7,600 per 1% share
- **COMP-0421:** 7,600 per 1% share

This metric reveals that some smaller institutions generate disproportionately high complaint rates relative to their customer base, suggesting either predatory practices targeting vulnerable populations or severe operational deficiencies.

**Response Performance by Company:** The detailed company table shows response times clustering around 13-17 days with response rates consistently above 90%, indicating industry-wide compliance with CFPB timelines but little competitive differentiation in service quality.

### 7. Submission Channel Insights

**Web referral dominates** as the fastest-response channel, processing complaints most efficiently. The distribution shows:
- **Web submissions:** 45,400 complaints (72.6% of total)
- **Referral:** 10,500
- **Phone:** 4,700
- **Postal mail:** 1,300
- **Fax/Email:** minimal

This heavy web skew suggests successful digital transformation of the complaint process but also raises accessibility concerns for less digitally-connected populations (elderly, rural, low-income consumers).

---

## Recommendations

### Recommendation 1: Launch Targeted Examination Initiative for Checking Account Operations

**Insight:** Checking/savings accounts generate 24,800 complaints (40% of total), with "deposits and withdrawals" as the top sub-issue at 5,600 complaints.

**Action:** The Supervision Division should immediately initiate a special examination program focused on transaction processing systems, fee disclosure practices, and account access procedures at the top 20 complaint-generating banks. Examinations should specifically assess:
- Real-time transaction processing capabilities
- Hold policies on deposited funds
- Overdraft fee calculation methodologies
- Mobile/online banking system reliability

**Expected Impact:** Reducing checking account complaints by 20% would eliminate 4,960 complaints annually, significantly improving consumer access to their own funds.

---

### Recommendation 2: Implement Escalated Enforcement for High Per-Capita Complaint Companies

**Insight:** COMP-0878 and COMP-0015 generate 7,500+ complaints per 1% market share, indicating severe consumer harm relative to their customer base.

**Action:** The Enforcement Division should fast-track investigations into the top 10 companies by per-capita complaint rate. These smaller institutions may be:
- Targeting vulnerable populations (elderly, immigrant communities, low-income consumers)
- Operating with inadequate compliance infrastructure
- Engaging in predatory lending or deceptive practices

Enforcement should prioritize consent orders requiring third-party monitoring, mandatory customer remediation, and enhanced supervision until complaint rates normalize to industry averages.

---

### Recommendation 3: Mandate Monetary Relief Justification for High-Denial Companies

**Insight:** Only 23.51% of complaints result in monetary relief, while 65.65% are closed with explanation only.

**Action:** For companies that deny monetary relief in >75% of complaints, the Policy Team should require detailed written justification for each denial to be submitted to CFPB within the complaint response. This creates an audit trail for:
- Identifying companies systematically denying valid claims
- Building enforcement cases for unfair claims practices
- Developing consumer education materials on effective complaint documentation

**Expected Impact:** Increased transparency pressure will likely increase monetary relief rates by 10-15 percentage points, translating to approximately $50-75M in additional consumer restitution annually (estimated).

---

### Recommendation 4: Develop State-Specific Consumer Education Campaigns for Low-Complaint Regions

**Insight:** Geographic distribution shows significant variations, with some states showing disproportionately low complaint volumes relative to population.

**Action:** The Consumer Education Office should partner with state attorneys general and community organizations in underrepresented states to:
- Conduct awareness campaigns about CFPB complaint channels
- Provide multilingual complaint filing resources
- Host community events at libraries, community centers, and senior facilities

Focus initially on rural Midwest and Mountain West states where complaint volumes appear artificially low.

---

### Recommendation 5: Establish "Managing an Account" Task Force for Product Simplification

**Insight:** "Managing an account" is the #1 reported issue at 15,100 complaints (24% of total), suggesting fundamental usability problems with basic banking products.

**Action:** Convene a cross-functional CFPB task force to:
- Analyze the 15,100 "managing an account" complaints to identify specific pain points
- Develop model disclosure forms for account terms, fees, and access procedures
- Create standardized account management guidelines for supervised institutions
- Publish consumer-facing guides on "Banking Basics" to set proper expectations

**Expected Impact:** Simplifying account management procedures could reduce this complaint category by 30% (4,500 complaints), improving basic banking accessibility for millions of consumers.

---

### Recommendation 6: Digitize Legacy Complaint Channels to Improve Resolution Speed

**Insight:** Web referral shows the fastest response times, while postal mail and phone channels lag.

**Action:** The Technology Office should develop:
- SMS-based complaint filing for mobile-primary consumers
- Voice-to-text AI for phone complaints to auto-populate web forms
- Multilingual chatbot interface for initial complaint triage

This ensures that consumers using slower channels still benefit from the efficiency of digital processing while maintaining accessibility for all demographics.

---

## Caveats and Assumptions

### Data Collection and Scope

This analysis covers consumer complaints submitted to the CFPB between **May 1, 2017, and August 28, 2023**. The sharp decline in complaints observed in August 2023 (717 vs. 1,749 peak) likely reflects incomplete data for the most recent period rather than a genuine trend reversal. All trend projections exclude the August 2023 data point to avoid skewing results.

### Data Cleaning Process

#### Step 1: Data Import & Initial Assessment
- Imported raw complaint data into Power BI from CFPB Consumer Complaint Database
- Verified 62,520 total records with no duplicate complaint IDs
- Confirmed date range coverage and identified 1,081 unique companies

#### Step 2: Handling Missing Values
- Sub-product classifications: 0.01% of complaints lacked sub-product detail—retained under parent product category
- Geographic data: All complaints contained state information with no missing values

#### Step 3: Metric Calculation
- **Timely Response Rate:** Percentage of complaints receiving company response within CFPB-mandated 15-day window (93.77% overall)
- **Complaints per 1% Market Share:** (Complaint Count / Market Share %) metric to normalize company performance across different institution sizes

### Key Assumptions

1. **Market share data accuracy:** Market_Share_Percent values represent each company's share of the consumer financial services market and sum to approximately 100% across all 1,081 companies. These percentages are assumed accurate and stable across the 2017-2023 analysis period.

2. **Timeliness definition:** The "Timely response?" field uses CFPB's regulatory standard (typically 15 calendar days). The 93.77% timely response rate reflects compliance with this threshold.

3. **Geographic attribution:** Complaints are mapped to consumers' state of residence using state centroid coordinates for visualization, not exact consumer locations.

4. **Response quality assessment:** "Company response to consumer" outcomes reflect final disposition but do not indicate whether resolutions were justified or satisfactory from the consumer's perspective.

### Analysis Limitations

- **Data completeness:** The sharp decline to 717 complaints in August 2023 (from a peak of 1,749) likely reflects incomplete data for the final reporting period rather than a genuine trend.

- **Complaint representativeness:** The dataset captures only consumers aware of CFPB channels who chose to file complaints. Populations experiencing issues but not complaining remain unmeasured, particularly in underrepresented states.

- **Company anonymization:** Company identifiers (COMP-0001 through COMP-1081) are anonymized for this analysis. Real-world enforcement would require mapping to actual institution names.

- **Market share normalization:** The Complaints_per_1pct_Share metric assumes linear relationships between market share and expected complaints. Companies serving higher-risk segments may naturally generate more complaints per market share point.

---

## Technical Implementation

### Power BI Features Utilized:
- **DAX measures** for KPI calculations (timely response rate, average response time, complaint growth rates)
- **Time intelligence functions** for trend analysis
- **Geographic mapping** with custom color scales for complaint density visualization
- **Drill-through pages** for detailed company and product-level exploration
- **Slicers** for interactive filtering by date range, product category, and state
- **Calculated columns** for per-capita metrics and response time categorizations

---

## Project Information

| Attribute | Details |
|-----------|---------|
| **Report Prepared By** | Uyi Godwin Omokaro |
| **Analysis Period** | May 2017 – August 2023 |
| **Dashboard Tool** | Microsoft Power BI Desktop |
| **Last Updated** | October 2025 |
| **Challenge** | Onyx Data Challenge October 2025 |

---

## Connect With Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/in/uyi-omokaro/)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?logo=github)](https://github.com/Uyi-Dave)
[![Portfolio](https://img.shields.io/badge/Portfolio-Visit-green)](https://github.com/Uyi-Dave)

---

*This analysis is submitted as part of the Onyx Data Challenge October 2025 and demonstrates real-world data analytics capabilities applicable to regulatory oversight, consumer protection policy development, and financial services examination prioritization.*
