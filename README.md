
E-Commerce Transaction Data Analysis

An end-to-end exploratory data analysis (EDA) project conducted in a VS Code Jupyter Notebook using Python and Pandas. This project evaluates business performance across five critical domains: sales trends, customer demographics, loyalty impact, geographical preferences, and operational fulfillment.

📊 Dataset Columns Reference

The analysis is performed on a standard retail dataset containing the following fields:
• Order Info: order_id, order_date, status, item_id, sku, qty_ordered, price, value, total, ref_num
• Promotions: discount_amount, Discount_Percent
• Customer Demographics & Loyalty: cust_id, Customer Since, age, Gender, full_name, E Mail, Phone No., SSN, User Name
• Geography: Place Name, County, City, State, Zip, Region
• Logistics & Payment: category, payment_method, bi_st, year, month

📈 The 5 Analytics Core Quizzes


Quiz 1: Revenue & Trend Analysis

• Objective: Map out monthly revenue fluctuations and pinpoint what product category drives the highest-performing month.
• Key Implementation: Standardised text fields into true datetime objects via pd.to_datetime(), normalised timestamps to standard year_month periods, and isolated peak historical periods to parse secondary category contributions.

Quiz 2: Customer Demographics & Loyalty Impact

• Objective: Group customer age values into discrete buckets to analyze Average Order Value (AOV) and product purchase volume while tracking customer retention value over time.
• Key Implementation: Implemented binning structures with pd.cut() to classify generations and tenure groups (loyalty_tier). Computed metrics simultaneously via multi-field .agg() routines, isolating individual shopping receipts using unique counts (nunique).

Quiz 3: Geographical Performance & Local Payment Landscapes

• Objective: Isolate the top three highest revenue-producing regions and discover the primary payment mechanism favored by local shoppers in those markets.
• Key Implementation: Evaluated individual geographic revenue contributions, compiled top tiers using .head(3), filtered parent records dynamically using .isin(), and iterated over subset matrices using logical loops to automatically flag specific regional transaction choices.

Quiz 4: Promotion & Discount Impact

• Objective: Evaluate whether promotional markdown tiers drive larger basket sizes or if they simply erode bottom-line margin.
• Key Implementation: Calculated mathematical linear trends utilizing the Pearson Correlation Coefficient formula (.corr()). Aggregated average purchase sizes across binned markdown percentages and mapped data arrays alongside a mathematical trendline using sns.regplot().

Quiz 5: Order Fulfillment & Operations

• Objective: Quantify business revenue leaks by calculating order failure rates (Cancellations and Returns) while identifying problematic stock items (SKUs) or payment gateways.
• Key Implementation: Extracted global operational health using normalised value counts, built string-matching filters to track problematic order states, and deployed custom lambda logic calculations to flag processing methods exhibiting abnormally high failure or fraud signatures.

🔑 Key Strategic Discoveries


1. High-Value Revenue Leakage & Operational Risks

• The Cancellation Emergency: Over 39.17% of all incoming orders are cancelled, representing a massive pipeline bottleneck.
• Premium SKU Leakage: A small handful of high-value items starting with the "MATSAM" prefix drive millions of shillings in lost value. For instance, SKU MATSAM5B10F7E2AC8C1 alone accounts for $6.54 Million in cancelled/returned orders.
• Broken Payment Channels: Digital payment options like bankalfalah (95.7% failure) and Easypay (82.5% failure) show catastrophic cancellation rates, highlighting deep technical integration glitches or heavy bot fraud attempts.

2. The Promotion & Markdown Paradox

• The Sweet Spot (11-20% Discounts): This markdown bucket serves as the most profitable promotional zone, generating $69.6 Million in net revenue across 48,120 unique orders while keeping a healthy balance between margin protection and volume.
• The Margin Eaters (51-75% Discounts): Deep markdowns successfully scale basket sizes up to 10.23 items per transaction, but trigger severe financial erosion. Total discounts given ($1.30M) vastly outpace the net revenue kept ($918k), creating high warehouse fulfillment overheads for minimal net return.

🛠️ Technology Stack & Libraries Used

• IDE: Visual Studio Code (VS Code)
• Environment: Jupyter Notebooks (.ipynb)
• Core Processing Data Library: Pandas
• Visualization Engine: Matplotlib & Seaborn
