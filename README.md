# SupplyGuard: Procurement, Supplier & Inventory Analytics Platform

## Executive Summary

SupplyGuard is an end-to-end data analytics project designed to help procurement teams monitor supplier performance, improve profitability, optimize inventory investments, and reduce operational risks.

Using procurement, vendor, sales, freight, and inventory data, the project answers critical business questions through descriptive and diagnostic analytics, enabling stakeholders to make data-driven procurement decisions.



# Business Problem

Procurement teams often struggle to identify:

* Supplier concentration risks
* Unprofitable vendor relationships
* Inventory overstocking
* Slow-moving inventory
* Freight cost inefficiencies
* Procurement decisions that negatively impact profitability

Without a centralized analytics solution, these issues can lead to reduced margins, excess working capital, and increased operational risk.



# Business Questions

1. Which vendors account for most procurement spend?
2. Which vendors generate the highest gross profit?
3. Why are certain vendors generating negative profit margins?
4. Which vendors demonstrate the most efficient inventory turnover?
5. Which products tie up the most inventory capital?
6. Which stores carry the highest inventory investment?
7. Are procurement volumes aligned with vendor profitability?
8. Are freight costs proportionate to procurement activity?



# Dataset Overview

The analysis was performed using procurement, supplier, inventory, and sales datasets containing:

* Vendor Information
* Purchase Transactions
* Sales Transactions
* Freight Costs
* Inventory Records
* Product Information
* Store Information



# Methodology

### Data Preparation

* Data ingestion using Microsoft Fabric Dataflows Gen2
* Data cleaning and transformation using PySpark
* Gold-layer analytical tables created for reporting

### Data Analysis

* Procurement Spend Analysis
* Vendor Profitability Analysis
* Inventory Analysis
* Inventory Turnover Analysis
* Freight Cost Analysis
* Supplier Risk Analysis

### Reporting

* Interactive Power BI Dashboards
* DAX Measures and KPIs
* Automated Refresh Pipelines
* Row-Level Security (RLS)



# Solution Architecture

```text
Source Data
    │
    ▼
Dataflows Gen2
    │
    ▼
Lakehouse (Silver Layer)
    │
    ▼
PySpark Transformations
    │
    ▼
Gold Analytical Tables
    │
    ▼
Semantic Model
    │
    ▼
Power BI Dashboard
    │
    ▼
Business Insights & Decisions
```



# Key Findings & Recommendations

## Q1. Which Vendors Account for Most Procurement Spend?

### Observation

Top 3 vendors—DIAGEO ($51M), MARTIGNETTI ($28M), and JIM BEAM ($24M)—account for 32.01% of the total procurement spend.

### Root Cause

Procurement activity is concentrated among a small group of strategic suppliers.

### Recommendation

Diversify supplier allocation and gradually reduce dependency on top vendors.

### Expected Business Impact

Reduce supplier concentration risk and improve supply continuity.



## Q2. Which Vendors Generate the Highest Gross Profit?

### Observation

DIAGEO, MARTIGNETTI, CONSTELLATION, and PERNOD RICARD contribute approximately 37% of total gross profit.

### Root Cause

Strong sales demand combined with efficient procurement relationships.

### Recommendation

Prioritize these vendors during procurement planning and contract negotiations.

### Expected Business Impact

Protect a significant portion of portfolio profitability.



## Q3. Why Are Certain Vendors Generating Negative Profit Margins?

### Observation

Several vendors operate at negative profit margins despite active sales volumes.

### Root Cause

High purchase costs and freight expenses reduce profitability.

### Recommendation

Review pricing agreements, freight contracts, and purchasing strategies.

### Expected Business Impact

Potential recovery of lost margin and improved profitability.



## Q4. Which Vendors Demonstrate the Most Efficient Inventory Turnover?

### Observation

BACARDI and JIM BEAM demonstrate the strongest inventory turnover performance.

### Root Cause

Higher demand and efficient inventory replenishment.

### Recommendation

Increase focus on high-turnover vendors while optimizing slow-moving inventory.

### Expected Business Impact

Reduced inventory carrying costs and improved inventory productivity.



## Q5. Which Products Tie Up the Most Inventory Capital?

### Observation

Jack Daniels, Grey Goose, Ketel One, and Jameson account for over $5M in inventory value.

### Root Cause

Large inventory positions relative to sales velocity.

### Recommendation

Optimize reorder points and replenishment policies.

### Expected Business Impact

Release working capital and improve inventory efficiency.



## Q6. Which Stores Carry the Highest Inventory Investment?

### Observation

A small number of stores account for a significant share of total inventory investment.

### Root Cause

Inventory allocation is heavily concentrated.

### Recommendation

Review replenishment policies and redistribute inventory where appropriate.

### Expected Business Impact

Reduce overstock risk and improve inventory utilization.



## Q7. Are Procurement Volumes Aligned with Vendor Profitability?

### Observation

Certain vendors receive high procurement volumes despite weak profitability.

### Root Cause

Procurement decisions focus on volume rather than margin performance.

### Recommendation

Introduce Profit Margin and Gross Profit per Unit as procurement KPIs.

### Expected Business Impact

Improve procurement effectiveness and portfolio profitability.



## Q8. Are Freight Costs Proportionate to Procurement Activity?

### Observation

Several high-spend vendors operate above the network freight benchmark.

### Root Cause

Shipment frequencies and freight agreements are not fully optimized.

### Recommendation

Review freight contracts and consolidate shipments where possible.

### Expected Business Impact

Reduce logistics costs and improve procurement efficiency.



# Dashboard Pages

### Page 1 – Procurement Analytics

* Procurement Spend
* Vendor Analysis
* Freight Analysis

### Page 2 – Inventory Analytics

* Inventory Value
* Product Analysis
* Store Analysis

### Page 3 – Supplier Performance Analytics

* Profitability Analysis
* Margin Analysis
* Inventory Turnover Analysis

### Page 4 – Business Insights & Recommendations

* Executive Summary
* Root Cause Analysis
* Recommended Actions
* Expected Business Impact



# Technology Stack

### Analytics

* Power BI
* DAX
* SQL
* PySpark

### Data Engineering

* Microsoft Fabric
* Dataflows Gen2
* Lakehouse
* Fabric Pipelines

### Governance

* Semantic Model
* Row-Level Security (RLS)



# Business Impact

* Identified supplier concentration risk where Top 3 vendors accounted for 32% of procurement spend.
* Uncovered negative-margin vendor relationships causing profit leakage.
* Identified inventory concentration across products and stores.
* Highlighted opportunities for freight cost optimization.
* Provided actionable recommendations to improve profitability, reduce supplier dependency, and optimize inventory investment.



# Dashboard Preview


### Business Performance Overview

<img width="1192" height="682" alt="image" src="https://github.com/user-attachments/assets/56d4db35-5d55-410a-bbf3-acfda80baee2" />


### Supplier Risk and vendor performance

<img width="1187" height="662" alt="image" src="https://github.com/user-attachments/assets/487200d7-2dbd-4bfb-aa06-8d144f146fb3" />


### Inventory & Procurement Optimization

<img width="1185" height="667" alt="image" src="https://github.com/user-attachments/assets/49c8d690-1c5f-4704-8bf4-d083d3d4b92e" />


### Business Insights Dashboard

<img width="1177" height="662" alt="image" src="https://github.com/user-attachments/assets/51a3debe-5894-4c71-a9f9-c06d98cdd7f2" />


### Fabric Pipeline

[<img width="1477" height="732" alt="Master Pipeline" src="https://github.com/user-attachments/assets/0a350d72-2833-4440-9b2a-09ac4bd474f1" />

### Semantic Model
<img width="1536" height="742" alt="Semantic Model" src="https://github.com/user-attachments/assets/8eb06998-eddd-4e01-96b6-d3d4d1fd8a13" />



# Future Enhancements

* Predictive Supplier Risk Scoring
* Vendor Performance Forecasting
* Inventory Demand Forecasting
* AI-Powered Procurement Assistant
* Automated Executive Summary Generation using Azure OpenAI
