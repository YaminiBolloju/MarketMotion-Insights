# A/B Testing for Marketing Campaign Optimization  

## Overview  
This project analyzes the effectiveness of two marketing campaigns (**Control Campaign vs. Test Campaign**) using **A/B testing techniques**. The dataset includes **advertising spend, impressions, reach, website clicks, searches, add-to-cart actions, and purchases**. The goal is to determine whether the test campaign leads to **better customer engagement and conversions** compared to the control group.  

## Dataset Description  
The dataset consists of two groups:  
- **Control Campaign**: The baseline marketing campaign.  
- **Test Campaign**: The experimental campaign being evaluated.  

### Features in the Dataset  
- **Campaign Name**: The name of the campaign.  
- **Date**: Date of the record.  
- **Spend [USD]**: Amount spent on the campaign.  
- **Impressions**: Number of times the ad was displayed.  
- **Reach**: Number of unique users who saw the ad.  
- **Website Clicks**: Number of clicks on the ad.  
- **Searches**: Users who searched for the product on the website.  
- **View Content**: Users who viewed products on the website.  
- **Add to Cart**: Users who added products to the cart.  
- **Purchases**: Number of completed purchases.  

## Project Workflow  

### 1. Data Import & Preprocessing  
- Downloaded datasets for **Control Group** and **Test Group**.  
- Combined both datasets into a single DataFrame.  
- Renamed columns for clarity.  
- Handled missing values (dropped a single missing row).  
- Converted **Date** column to datetime format.  

### 2. Exploratory Data Analysis (EDA)  
- **Summary Statistics**: Compared key metrics between the two campaigns.  
- **Correlation Analysis**:  
  - **Ad Spend vs. Purchases**: Weak correlation (0.031), suggesting inefficient budget allocation.  
  - **Searches vs. View Content**: Strong correlation (0.89), indicating that searchers engage with product pages.  
  - **Add to Cart vs. Purchases**: Moderate correlation (0.39), highlighting cart abandonment issues.  
  - **Website Clicks vs. Purchases**: Weak correlation (~0.03), suggesting landing pages need improvement.  

### 3. Distribution Analysis  
- **Violin Plots** were used to analyze the spread of campaign performance.  
- Observations:  
  - Test campaign had **lower variability in searches and view content**, meaning more consistent engagement.  
  - Higher spend in the **test campaign did not translate into more purchases**.  
  - Control campaign had a **higher spread in impressions and clicks**, reaching a broader but less engaged audience.  

### 4. Normality & Hypothesis Testing  
- **Shapiro-Wilk Test**: Checked for normality in numeric variables.  
- **A/B Testing Using t-tests and Mann-Whitney U tests**:  
  - **Spend [USD]**: Test campaign had **statistically higher spend** than the control.  
  - **Purchases**: No significant difference between the two campaigns.  
  - **Reach, Website Clicks, Searches, Add to Cart**: Tested for significant differences between campaigns.  

## Key Findings & Conclusions  
- **Spending More Did Not Significantly Increase Purchases**: Despite the test campaign spending more, it did not lead to higher conversion rates.  
- **Cart Abandonment Is a Concern**: Moderate correlation between "Add to Cart" and "Purchases" suggests a need for checkout process optimization.  
- **Landing Page & Call-to-Action (CTA) Optimization Needed**: Low correlation between website clicks and purchases indicates traffic is not effectively converting.  
- **Search and View Content Engagement Is Strong**: Users who search for products are more likely to engage, but many do not complete purchases.  

## Next Steps  
- **Optimize Ad Spend**: Allocate budget more effectively based on performance insights.  
- **Improve Checkout Experience**: Reduce cart abandonment through incentives and UX enhancements.  
- **Refine Targeting Strategy**: Use segmented audiences to improve reach and engagement.  
- **A/B Test Landing Pages**: Experiment with different CTA placements and content structures.  

## Author  
Rajkumar Shenigaram  
