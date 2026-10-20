
🛒 E-Commerce Transaction Insights Hub

An advanced forensic data analysis framework engineered inside VS Code Jupyter Notebooks to diagnose leaks and growth opportunities in a retail pipeline. By answering 5 core business puzzles, this project uncovers massive operational vulnerabilities and isolates a multi-million dollar promotion paradox.

🗺️ Framework Overview

This project bypasses basic data metrics to evaluate five interconnected pillars of retail performance:
📦 DATA INPUT ──► 💸 1. Revenue Trends ──► 👥 2. Loyalty Cohorts ──► 📍 3. Regional Landscapes ──► 🏷️ 4. Discount Impacts ──► 🚨 5. Order Failures

📈 The 5 Core Analytical Pillars


💰 1. Revenue & Seasonal Trend Analysis

• Core Task: Pinpoint historically dominant sales months and map the exact categories fueling those transaction surges.
• Technique: Standardised raw text into true datetimes (pd.to_datetime), parsed them into standard chronological periods, and deployed targeted sub-filtering workflows.

👥 2. Demographics & Loyalty Lifespans

• Core Task: Benchmark Average Order Value (AOV) against generational buckets and long-term customer lifespans.
• Technique: Cut continuous raw ages into discrete groups with pd.cut() and tracked multi-dimensional metrics using combined .agg() logic.

📍 3. Regional Performance & Payment Landscapes

• Core Task: Isolate top-tier geographic zones and trace the specific payment methods preferred by high-volume local buyers.
• Technique: Ranked top geographic performers with .head(3), created array matches with .isin(), and used iteration loops to uncover payment patterns.

🏷️ 4. The Promotion & Discount Paradox

• Core Task: Evaluate whether deep markdowns actually expand shopping baskets or if they just damage margins.
• Technique: Ran mathematical linear trends via Pearson Correlation (.corr()), grouped fragmented fractions into distinct discount tiers, and plotted trends with sns.regplot().

🚨 5. Order Fulfillment & System Leakage

• Core Task: Map operational revenue loss by tracking order cancellations, returns, high-risk items, and faulty payment processors.
• Technique: Mapped operational health with normalized string counters, isolated failed states, and engineered custom lambda functions to flag transaction failure rates.

🔑 Critical Discoveries & Business Intelligence


💸 The Promotion Paradox: The 11–20% Sweet Spot

The data uncovers a striking trend: as discounts scale up, order sizes jump but total revenue drops significantly.
• The Engine (11–20% Tiers): This represents the most profitable promotional zone, bringing in $69.6 Million across 48,120 transactions while safely protecting brand value.
• The Margin Eaters (51–75% Tiers): Deep markdowns increase basket sizes to an average of 10.23 items, but cause severe revenue loss. Total markdown value given ($1.30M) completely outpaced the net revenue kept ($918k), creating high warehouse fulfillment costs for minimal return.

🚨 The Operational Crisis: Broken Checkout Channels

• The Cancellation Spike: Over 39.17% of all incoming transactions are cancelled, pointing to major bottlenecks or system glitches.
• Premium SKU Leakage: A small handful of high-value items starting with the "MATSAM" prefix drive millions of dollars in lost value. For instance, SKU MATSAM5B10F7E2AC8C1 alone accounts for $6.54 Million in cancelled/returned orders.
• Broken Gateways: Digital wallets like bankalfalah (95.7% failure) and Easypay (82.5% failure) show catastrophic cancellation rates, highlighting deep technical integration glitches or heavy bot fraud attempts.

🛠️ Data Infrastructure

• Engine: Python 3.8+ [1]
• Data Processing: Pandas (Advanced Grouping, Aggregation, and Binning) [2]
• Visualization: Matplotlib & Seaborn (Dual-Axis Charts, Trendplots)
🛠️ Technology Stack & Libraries Used

• IDE: Visual Studio Code (VS Code)
• Environment: Jupyter Notebooks (.ipynb)
• Core Processing Data Library: Pandas
• Visualization Engine: Matplotlib & Seaborn
