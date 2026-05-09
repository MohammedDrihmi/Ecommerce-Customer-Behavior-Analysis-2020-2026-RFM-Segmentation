# 📊 E-Commerce RFM Customer Segmentation Analysis

> A full-stack customer intelligence project built entirely in Microsoft Excel — turning 6 years of raw transaction data into 11 actionable customer segments, 6 analytical dimensions, and a clear revenue strategy.

---

## 🗂️ Table of Contents

- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Customer Segments](#customer-segments)
- [Key Findings](#key-findings)
- [Recommendations](#recommendations)
- [Tools & Skills](#tools--skills)
- [File Structure](#file-structure)
- [How to Use](#how-to-use)
- [Author](#author)

---

## Project Overview

This project applies **RFM (Recency, Frequency, Monetary)** analysis to a global e-commerce dataset spanning **6 years (2020–2026)**. The entire analysis was built natively in **Microsoft Excel** using Excel Formulas & Functions ,pivot tables,and pivot charts.

The goal was to move beyond surface-level sales metrics and build a structured understanding of **who the customers are**, **how they behave**, and **what the business should do** — segment by segment.

| Dimension | Detail |
|-----------|--------|
| Customers analyzed | 8,000 |
| Time period | 2020 – 2026 |
| Total revenue | $1.14 Billion |
| Customer segments | 11 |
| Countries | 20 |
| Acquisition channels | 6 |

---

## Problem Statement

An e-commerce business with 6 years of transaction history had **no structured view of its customer base**. Without a segmentation model, every customer was treated the same — resulting in:

- Generic marketing campaigns sent to every customer regardless of value
- Missed retention windows for high-value customers going cold
- Budget wasted on low-return segments
- Decisions based on intuition rather than data

**7 critical business questions were identified:**

1. Who are the most valuable customers, and how can the business retain them?
2. Who are the potential loyalists — and what does it take to convert them?
3. Which customers are at risk of churning, and what strategies can bring them back?
4. How do gender and age influence shopping behavior and engagement?
5. How does newsletter subscription influence purchase frequency and spend?
6. Is there a relationship between acquisition channel and customer quality?
7. How can the business transform one-time buyers into loyal, repeat customers?

---

## Dataset

The dataset contains anonymized e-commerce transaction records with the following fields:

| Field | Description |
|-------|-------------|
| `customer_id` | Unique customer identifier |
| `transaction_date` | Date of purchase |
| `order_value` | Value of each order (USD) |
| `total_orders` | Cumulative order count per customer |
| `total_spend_usd` | Lifetime spend per customer |
| `days_since_last_purchase` | Recency metric |
| `acquisition_channel` | How the customer was acquired |
| `newsletter_subscribed` | Boolean subscription status |
| `country` | Customer location |
| `gender` | Customer gender |
| `age_group` | Age band (18-24, 25-34, 35-44, 45-54, 55-64, 65+) |
| `preferred_category` | Top product category |

---

## Methodology

### Step 1 — Data Cleaning
Raw data was cleaned and standardized using **Power Query** in Excel: removing duplicates, handling nulls, standardizing date formats, and normalizing spend values.

### Step 2 — RFM Scoring
Each customer was scored across three dimensions using **percentile-based quintile ranking (1–5)**:

| Score | Dimension | Question |
|-------|-----------|----------|
| **R** | Recency | How recently did the customer purchase? |
| **F** | Frequency | How often do they buy? |
| **M** | Monetary | How much do they spend in total? |

Scores were combined into a **3-digit RFM code** (e.g., `555` = perfect Champion, `111` = Lost).

### Step 3 — Segmentation
11 customer segments were defined by mapping RFM score patterns to business-meaningful labels using a lookup logic table in Excel.

### Step 4 — Pivot Table Analysis
Six analytical pivot tables were built to analyze segments across:
- Revenue contribution and customer share
- Newsletter behavior and subscriber lift
- Acquisition channel quality
- Age group distribution and spend
- Gender behavior differences
- Recency and order frequency patterns

### Step 5 — Business Recommendations
Each segment received a tailored action plan based on its data profile — from VIP retention strategies for Champions to low-cost re-engagement for Hibernating customers.

---

## Customer Segments

| Segment | Customers | Revenue Share | Priority |
|---------|-----------|---------------|----------|
| Champion | 7.5% | 22% | 🟢 Retain |
| Loyal Customer | 10.2% | 22.4% | 🟢 Grow |
| Cannot Lose Them | 2.9% | 7.4% | 🟠 Urgent |
| At Risk | 15.6% | 24.7% | 🔴 Critical |
| Need Attention | 8.2% | 8.4% | 🟠 Watch |
| Potential Loyalist | 15% | 6.1% | 🔵 Convert |
| Promising | 4.7% | 2.4% | 🔵 Nurture |
| New Customer | 10.8% | 1.1% | 🔵 Onboard |
| Hibernating | 18.6% | 4.9% | ⚪ Selective |
| About To Sleep | 4.1% | 0.5% | ⚪ Low |
| Lost | 2.5% | 0.2% | ⚪ Deprioritize |

---

## Key Findings

### 1. Revenue Is Dangerously Concentrated
**17.6% of customers (Champions + Loyal) generate 44.5% of total revenue.** The business is heavily dependent on a small elite segment. Losing even a fraction of these customers has an outsized revenue impact.

### 2. The Biggest Revenue Risk: At Risk Segment
**At Risk customers (15.6% of base) account for 24.7% of total revenue — $281.9M.** With an average of 113 days since their last purchase, this is the single greatest retention vulnerability in the business.

### 3. Silent VIPs: Cannot Lose Them
**232 customers averaging $365,123 in lifetime spend** haven't purchased in 182 days on average. This tiny segment holds $84.7M in revenue. They are the highest-value recovery opportunity.

### 4. Newsletter Has Reach But No Revenue Impact
**61.7% of customers are subscribed**, yet the spending difference between subscribers and non-subscribers is only **+0.23%**. The newsletter functions as a broadcast channel, not a personalized retention engine.

### 5. Acquisition Channel Quality Varies Significantly
- **Direct** (10.3% of customers) delivers the **highest average spend at $151K**
- **Organic Search** (27.4% of customers) offers the best **scale-to-quality balance at $141K**
- **Social Media** (21.9% of customers) produces the **lowest average spend at $135K** — volume without value

### 6. Ages 25–44 Power the Revenue Engine
The **25–44 age band represents 59.6% of customers** and drives the majority of revenue. The **55–64 group**, while only 4.7% of customers, shows the **highest average spend ($144K)** — an underleveraged premium niche.

### 7. Gender as a Behavioral Layer
- **Female customers (51.7%)** show stronger repeat purchase frequency (16.76 avg orders)
- **Male customers (48.3%)** show a slightly higher average spend ($143.6K vs $140.8K)

---

## Recommendations

| Priority | Action | Segment | Urgency |
|----------|--------|---------|---------|
| 01 | Personalized win-back campaigns | At Risk | Immediate |
| 02 | VIP reactivation outreach | Cannot Lose Them | Immediate |
| 03 | VIP exclusivity & early access programs | Champions | Ongoing |
| 04 | Loyalty tier progression & repeat nudges | Potential Loyalists | Medium-term |
| 05 | Scale SEO investment aggressively | Organic Search | Ongoing |
| 06 | Shift newsletter from broadcast to lifecycle campaigns | All segments | Medium-term |

---

## Tools & Skills

| Tool / Skill | Usage |
|---|---|
| **Microsoft Excel** | Full analysis environment |
| **Power Query** | Data cleaning & transformation |
| **Pivot Tables** | Multi-dimensional segment analysis |
| **RFM Modeling** | Customer segmentation framework |
| **Business Intelligence** | Insight generation & recommendation design |
| **Data Storytelling** | Executive presentation & narrative |

---

## File Structure

```
📁 ecommerce-customer-behavior-analysis-2020-2026-RFM segmentation/
│
├── 📊 Ecommerce_RFM_Analysis.xlsx        # Main Excel workbook
│   ├── Sheet: Customer Data              # Raw & cleaned dataset
│   ├── Sheet: RFM Score                  # Scoring model & segment mapping
│   ├── Sheet: Overview                   # Segment summary pivot table
│   ├── Sheet: Newsletters                # Newsletter behavior analysis
│   ├── Sheet: Acquisition                # Channel quality analysis
│   ├── Sheet: Age                        # Age group deep-dive
│   └── Sheet: Gender                     # Gender behavior analysis
│
├── 📑 Licence                            # MIT Licence
├── 📄 README.md                                  # This file
└── 📑 RFM_Customer_Segmentation_Analysis.pptx   # presentation
```

---

## How to Use

1. **Clone or download** this repository
2. Open `Ecommerce_RFM_Analysis.xlsx` in Microsoft Excel (2016 or later recommended)
3. Navigate through the sheets in order — start with **Customer Data**, then **RFM Score**, then the analytical sheets
4. The **Overview** sheet provides the executive summary pivot table
5. Each analytical sheet contains an embedded insight & recommendation text box
6. Review the **presentation file** for a slide-by-slide narrative of the findings

> **Note:** Power Query connections are embedded in the workbook. If prompted, click *Enable Content* to allow data refresh.

---

## About Me :

**Mohammed Drihmi** — Data Analyst

Passionate about turning raw data into business decisions. This project demonstrates end-to-end analytical thinking: from data cleaning and model design to segmentation, insight generation, and executive communication.

---

*Built entirely in Microsoft Excel · 2020–2026 E-Commerce Dataset · 8,000 Customers · 11 Segments*
