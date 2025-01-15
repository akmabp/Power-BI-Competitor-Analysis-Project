# Power BI Competitor Analysis Project

## Description:
This project focuses on competitor analysis by visualizing and analyzing sales trends across all regions. The goal is to provide insights into Sintec's performance compared to its competitors, highlighting key metrics such as revenue growth, market share, and top-performing products.

## Key Objectives:
- **Competitor Analysis**: Compare Sintec's sales trends against major competitors and analyze sales across various regions.
- **Revenue Share Analysis**: Display top manufacturers by revenue share across regions to understand the competitive landscape.
- **Sales Growth**: Examine sales growth over time and compare it to the previous year's performance.
- **Market Share**: Identify Sintec's market share in comparison to key competitors in various regions.

## Tools & Technologies:
- **Power BI**: Used to create visualizations, KPIs, and interactive reports.
- **DAX (Data Analysis Expressions)**: Utilized for calculating running totals and comparing performance over time.

## Key Features:
1. **Running Total Sales**: 
    ```DAX
    CALCULATE(
        SUM([Sales]),
        DATESMTD([Date]) 
    )
    ```
    This calculation computes running total sales for each month, resetting every month.

2. **Year-over-Year Sales Comparison**:
    ```DAX
    CALCULATE(
        SUM('Sales'[Revenue]),
        SAMEPERIODLASTYEAR('Date'[Date])
    )
    ```
    This formula calculates revenue compared to the same period last year.

3. **Top 5 Manufacturers by Revenue**: 
    The report filters and displays the top 5 manufacturers by revenue, using a tree map to visually represent their market share.

4. **Key Performance Indicators (KPIs)**: 
    KPIs are calculated to show sales growth and the rate at which revenue is increasing during a fixed period.

5. **Market Share Analysis**: 
    Conditional formatting is applied to highlight manufacturers' performance, market share, and growth.

## Insights:
- **Sintec's Market Share**: Sintec holds 38.22% of the market share in the USA, outperforming other manufacturers.
- **Top Growth**: Q1 2021 saw the highest growth at 18.8% compared to the previous year.
- **Key Competitor**: Artisans is Sintec's primary competitor in Germany, holding over 50% of the market share.
- **Global Growth**: Sintec's global market share stands at 21.15%, showing strong revenue growth relative to competitors.

## Top Performing Products:
The analysis identifies the best-performing segments and products, enabling Sintec to focus on consistent revenue generators and drive further growth.

## Final Deliverables:
An interactive Power BI report was developed for Sintec's executive team, enabling them to:
- Perform deep dives into historical sales data.
- Gain advanced insights on market performance.
- Make informed decisions to improve sales and market positioning against competitors.
