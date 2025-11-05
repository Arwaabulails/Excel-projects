# 📊 Telco Customer Churn Analysis

![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Data Analysis](https://img.shields.io/badge/Data_Analysis-4285F4?style=for-the-badge&logo=google-analytics&logoColor=white)
![Dashboard](https://img.shields.io/badge/Dashboard-FF6B6B?style=for-the-badge&logo=tableau&logoColor=white)

> A comprehensive Excel-based analysis identifying customer churn patterns and revenue optimization opportunities in the telecommunications industry.

## 🎯 Project Overview

This project analyzes **7,043 customer records** from a telecommunications company to uncover the key drivers of customer churn and provide actionable recommendations for retention strategies. Using advanced Excel techniques including pivot tables, VLOOKUP, and interactive dashboards, the analysis reveals critical insights that could save **$840K-$1.68M annually**.

### 📈 Key Findings

- **26.5%** overall customer churn rate
- **42.7%** churn rate for month-to-month contracts (15x higher than two-year contracts)
- **$139,000** monthly revenue loss from churned customers
- **47.7%** of new customers (0-12 months) churned within their first year
- **41.9%** churn rate among fiber optic service users

## 🛠️ Tools & Technologies

- **Microsoft Excel** - Primary analysis tool
- **Pivot Tables** - Multi-dimensional data analysis
- **Advanced Excel Functions** - VLOOKUP, SUMIF, COUNTIF, AVERAGEIF, nested IF statements
- **Data Visualization** - Interactive charts and KPI dashboards
- **DAX-style Formulas** - Custom calculated columns

## 📁 Project Structure

```
telco-customer-churn-analysis/
│
├── data/
│   └── telco_customer_churn.csv          # Original dataset (7,043 records)
│
├── analysis/
│   ├── telco_churn_analysis.xlsx         # Main analysis workbook
│   └── dashboard.xlsx                     # Interactive dashboard
│
├── documentation/
│   ├── telco_customer_churn_project.pdf  # Detailed project report
│   └── methodology.md                     # Analysis methodology
│
├── images/
│   ├── dashboard_screenshot.png
│   ├── churn_by_contract.png
│   └── revenue_impact.png
│
└── README.md
```

## 🔍 Analysis Methodology

### 1. Data Cleaning & Preparation
- Removed duplicates and handled missing values (11 blanks in TotalCharges)
- Converted data types for accurate calculations
- Created calculated columns (Tenure_Group, Revenue_Category, Customer_Value)
- Applied Excel Table formatting for structured references

### 2. Exploratory Data Analysis
- **Churn Rate by Contract Type**: Identified month-to-month contracts as highest risk
- **Tenure Analysis**: Discovered first-year customers have 47.7% churn rate
- **Service Type Impact**: Found fiber optic users churn 2.2x more than DSL
- **Revenue Segmentation**: Analyzed monthly charges vs. churn correlation

### 3. Advanced Analysis Techniques
```excel
# Tenure Grouping Formula
=IF([@Tenure]<=12,"0-12",IF([@Tenure]<=24,"13-24",
  IF([@Tenure]<=36,"25-36",IF([@Tenure]<=48,"37-48","49+"))))

# VLOOKUP for Price Comparison
=VLOOKUP([@InternetService], InternetPricing, 2, FALSE)

# Churn Rate Calculation
=COUNTIF(tbl_Churn[Churn],"Yes")/COUNTA(tbl_Churn[CustomerID])
```

### 4. Interactive Dashboard
- **KPI Cards**: Total customers, churn rate, revenue loss, average tenure
- **Dynamic Charts**: Churn by contract, tenure, service type, demographics
- **Slicers**: Interactive filtering by contract type, internet service, gender
- **Insights Panel**: Key findings and recommendations

## 📊 Key Insights

### 🔴 High-Risk Segments

| Segment | Churn Rate | Revenue Impact |
|---------|-----------|----------------|
| Month-to-Month Contracts | 42.7% | $122K/month |
| First Year Customers (0-12 months) | 47.7% | $77K/month |
| Fiber Optic Users | 41.9% | $96.5K/month |
| Customers without Partners | 33.0% | High |

### 💰 Revenue Impact

- **Total Monthly Revenue**: $456,000
- **Monthly Revenue Loss**: $139,000 (30.5% at risk)
- **Average Monthly Charge (Churned)**: $74.44
- **Average Monthly Charge (Active)**: $61.27

### 📉 Customer Tenure Patterns

```
Tenure Range    | Total | Churned | Churn Rate
----------------|-------|---------|------------
0-12 months     | 2,186 |  1,037  |   47.7%
13-24 months    | 1,024 |    294  |   28.7%
25-36 months    |   832 |    180  |   21.6%
37-48 months    |   762 |    145  |   19.0%
49+ months      | 2,239 |    213  |    9.5%
```

## 💡 Strategic Recommendations

### 🎯 Priority 1: Contract Optimization
- **Action**: Offer 15-20% discount for annual contract upgrades
- **Target**: Month-to-month customers with 6+ months tenure
- **Expected Impact**: Reduce churn from 42.7% to 30%
- **Projected Savings**: $35K-$45K monthly

### 🎯 Priority 2: First-Year Retention Program
- **Action**: Implement new customer onboarding and 6-month check-ins
- **Target**: Customers in their first 12 months
- **Expected Impact**: Reduce first-year churn by 20%
- **Projected Savings**: $15K monthly

### 🎯 Priority 3: Fiber Optic Service Improvement
- **Action**: Investigate service quality issues and competitive pricing
- **Target**: Fiber optic customers with high monthly charges
- **Expected Impact**: Reduce fiber churn from 41.9% to 30%
- **Projected Savings**: $25K-$30K monthly

### 🎯 Priority 4: Engagement & Bundling Strategy
- **Action**: Promote service bundles and multi-product subscriptions
- **Target**: Low-engagement customers with 1-2 services only
- **Expected Impact**: Increase customer stickiness by 25%

## 📈 Business Value

### Immediate Impact
✅ Identification of highest-risk customer segments  
✅ Prioritized action plan with ROI estimates  
✅ Interactive dashboard for ongoing monitoring  
✅ Foundation for predictive churn modeling  

### Long-Term Strategic Value
🎯 **Potential churn reduction**: 10 percentage points (26.5% → 16.5%)  
🎯 **Customers saved**: 700+ annually  
🎯 **Revenue protected**: $840K-$1.68M+ annually  
🎯 **Improved customer satisfaction** and competitive advantage  

## 🚀 Getting Started

### Prerequisites
- Microsoft Excel 2016 or later
- Basic understanding of Excel functions and pivot tables

### Usage
1. **Clone the repository**
   ```bash
   git clone https://github.com/Arwaabulails/telco-churn-analysis.git
   ```

2. **Open the analysis workbook**
   - Navigate to `analysis/telco_churn_analysis.xlsx`
   - Enable macros if prompted

3. **Explore the dashboard**
   - Use slicers to filter data by different segments
   - Review KPI cards for key metrics
   - Analyze charts for visual insights

4. **Review methodology**
   - Check `documentation/telco_customer_churn_project.pdf` for detailed analysis

## 📚 Dataset Information

- **Source**: [Kaggle - Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Records**: 7,043 customers
- **Variables**: 21 columns
- **Target Variable**: Churn (Yes/No)

### Key Variables
- **Customer Demographics**: Gender, SeniorCitizen, Partner, Dependents
- **Account Information**: Tenure, Contract, PaymentMethod, MonthlyCharges, TotalCharges
- **Services**: PhoneService, InternetService, OnlineSecurity, TechSupport, StreamingTV, etc.

## 🎓 Skills Demonstrated

### Technical Skills
✔️ Data Cleaning & Quality Assurance  
✔️ Advanced Excel Functions (VLOOKUP, SUMIF, COUNTIF, nested IF)  
✔️ Pivot Table Analysis & Data Summarization  
✔️ Interactive Dashboard Design  
✔️ Data Visualization Best Practices  
✔️ KPI Development & Tracking  

### Analytical Skills
✔️ Business Problem Decomposition  
✔️ Pattern Recognition & Insight Extraction  
✔️ Root Cause Analysis  
✔️ ROI Calculation & Financial Impact Assessment  
✔️ Data-Driven Decision Making  

### Business Skills
✔️ Customer Retention Analysis  
✔️ Revenue Impact Quantification  
✔️ Strategic Recommendation Development  
✔️ Stakeholder Communication  
✔️ Professional Report Writing  

## 🏆 Project Achievements

- ✅ Analyzed 7,043+ customer records with 99.8% data quality
- ✅ Identified $139K monthly revenue at risk
- ✅ Developed 4 strategic retention initiatives
- ✅ Created interactive dashboard with 10+ visualizations
- ✅ Projected $840K-$1.68M potential annual savings
- ✅ Documented complete analysis methodology

## 📝 Lessons Learned

### Key Takeaways
1. **Data quality is foundational** - Clean data is essential for reliable insights
2. **Context matters** - Understanding business context transforms data into intelligence
3. **Simplicity beats complexity** - Clear visualizations are more effective than cluttered dashboards
4. **Iteration improves outcomes** - Testing and refinement are essential

### Challenges Overcome
- Handled missing values contextually (new customers with zero tenure)
- Converted data types for accurate calculations
- Created meaningful tenure categories through iterative testing
- Balanced information density with dashboard clarity

## 📧 Contact

**Arwa Mustafa Abu-Laila**  
📧 Email: abulailaarwa71@gmail.com  
💼 LinkedIn: [linkedin.com/in/arwa-abulaila-7a2562251](https://www.linkedin.com/in/arwa-abulaila-7a2562251/)  
🐙 GitHub: [@Arwaabulails](https://github.com/Arwaabulails)

## 📄 License

This project is available for educational and portfolio purposes.

---

