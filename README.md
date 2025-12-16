# Dynamic Pricing Strategy – Data-Driven Pricing Project

## Overview
This project focuses on building a **practical, data-driven pricing strategy** for a consumer brand selling products on online marketplaces. The goal was to move away from reactive pricing decisions and design a **structured pricing framework** that balances profitability, demand behavior, inventory health, and market competition.

The project is designed to reflect how pricing decisions are made in real-world operations teams, using imperfect and incomplete data, while still producing reliable and actionable outputs.

---

## Problem Context
In many marketplace-driven businesses, pricing is often adjusted based on short-term signals without a clear framework. This can lead to issues such as:
- Products selling too quickly and creating inventory pressure  
- Slow-moving inventory despite marketing spend  
- Prices drifting away from competitor benchmarks without clear justification  

This project addresses these challenges by creating a **rule-based pricing engine** that generates consistent, explainable price recommendations at the SKU level.

---

## Data Used
Multiple datasets were combined to simulate a realistic pricing environment:

- **Pricing Data** – Product cost, fulfillment fees, storage and handling costs, and margin thresholds  
- **Historical Sales Data** – Page views and units ordered to understand demand and conversion behavior  
- **Inventory Health Data** – Days of supply and weeks of inventory cover to identify overstock or stock risk  
- **Competitor Data** – Average competitor pricing to maintain market alignment  

The datasets intentionally include missing and inconsistent values to mirror real marketplace data.

---

## Pricing Strategy Approach
The pricing logic was built in clear, sequential layers:

1. **Cost and Margin Foundation**  
   Each SKU’s landed cost is calculated, followed by a minimum acceptable price and a target price based on margin expectations.

2. **Inventory-Based Adjustments**  
   Prices are adjusted downward for overstocked items to improve sell-through, and upward for low-stock items to protect availability.

3. **Demand-Based Adjustments**  
   Conversion performance is used as a demand signal to fine-tune pricing—softening prices for weak conversion and strengthening prices when demand is strong.

4. **Market Alignment**  
   Recommended prices are kept within a reasonable range of competitor benchmarks to avoid unjustified premiums.

5. **Final Guardrails**  
   Every recommendation is validated to ensure it does not fall below the minimum margin threshold.

---

## Handling Real-World Data Challenges
Instead of dropping SKUs due to missing values, the project applies **business-safe defaults** for margins and costs. This approach ensures:
- No pipeline failures
- Continuous price recommendations
- Greater operational realism

This reflects how analytics is often handled in production environments.

---

## Outputs
The project produces:
- **SKU-level recommended prices**
- An **operations-ready CSV pricing playbook** that can be reviewed by business or category teams
- **Visual diagnostics** that help validate pricing behavior, including:
  - Recommended price vs market price
  - Distribution of price changes across SKUs

These outputs are designed to be understandable and actionable for non-technical stakeholders.

---

## Tools & Technologies
- Python (Pandas, NumPy, Matplotlib)
- Jupyter Notebook
- CSV-based data processing and outputs

---

## What This Project Demonstrates
- Translating analytical logic into real business decisions  
- Building pricing systems that are explainable and scalable  
- Working with imperfect data in a structured and thoughtful way  
- Applying an operations-focused mindset to analytics problems  

---

## Author
**Sai Balaji**  
Aspiring Data Analyst | Project-driven | Interested in solving real-world business problems using data
