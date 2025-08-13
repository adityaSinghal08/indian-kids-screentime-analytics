# Indian Kids Screen Time Analytics Dashboard 📊

Interactive dashboard analyzing screen time patterns and health impacts among Indian children, with demographic breakdowns by age, gender, and residence area.

## 🎯 Project Overview

This comprehensive analytics dashboard examines digital wellness among Indian children, providing stakeholders with actionable insights into media consumption habits and their associated health impacts. The dashboard enables data-driven decision making for parents, educators, healthcare professionals, and policy makers.

## 📁 Repository Structure

```
indian-kids-screentime-analytics/
├── dashboard-images/           # Dashboard screenshots and visualizations
├── README.md                   # Project documentation
├── clean-data.xlsx            # Processed and transformed dataset
├── complete-analytics.xlsx    # Comprehensive analysis workbook
│                             # (Contains: original data, cleaned data, 
│                             #  planning sheets, pivot tables, dashboard)
├── original-data.xlsx         # Raw dataset before transformation
└── project-overview.pdf       # Detailed project documentation
```

## 🔧 Data Transformation Process

### Original Data Format
The raw dataset contained the following structure:
```
Age | Gender | Avg_Daily_Screen_Time_hr | Primary_Device | Exceeded_Recommended_Limit | Educational_to_Recreational_Ratio | Health_Impacts | Urban_or_Rural
```

**Example Original Record:**
```
14 | Male | 3.99 | Smartphone | TRUE | 0.42 | Poor Sleep, Eye Strain | Urban
```

### Data Cleaning & Transformation

#### 1. **Age Grouping**
- **Transformation:** Converted individual ages into meaningful age groups
- **Purpose:** Enable demographic analysis and pattern recognition
- **Implementation:** Created age ranges (e.g., 6-8, 9-11, 12-14, 15-17)

#### 2. **Screen Time Range Categorization**
- **Transformation:** Converted continuous screen time values into discrete ranges
- **Original:** `Avg_Daily_Screen_Time_hr: 3.99`
- **Transformed:** `Daily Screen Time Range: 3.5-4`
- **Purpose:** Simplify analysis and align with health recommendation guidelines

#### 3. **Primary Content Classification**
- **Transformation:** Derived content type from Educational_to_Recreational_Ratio
- **Logic:** 
  - If `Educational_to_Recreational_Ratio > 0.5` → `Primary Content: Educational`
  - If `Educational_to_Recreational_Ratio ≤ 0.5` → `Primary Content: Recreational`
- **Example:** `0.42 ratio → Recreational content`

#### 4. **Health Issues Separation**
- **Transformation:** Split comma-separated health issues into individual boolean columns
- **Original:** `Health_Impacts: "Poor Sleep, Eye Strain"`
- **Transformed:** 
  - `Sleep Issues: TRUE`
  - `Eye Strain: TRUE`
  - `Anxiety: FALSE`
  - `Obesity: FALSE`
- **Purpose:** Enable granular health impact analysis and correlation studies

#### 5. **Standardized Naming**
- **Residence Area:** `Urban_or_Rural` → `Residence Area`
- **Limit Compliance:** `Exceeded_Recommended_Limit` → `Over Limit`

### Cleaned Data Format
```
Age Group | Gender | Daily Screen Time Range | Primary Device | Over Limit | Primary Content | Residence Area | Sleep Issues | Eye Strain | Anxiety | Obesity
```

**Example Cleaned Record:**
```
12-14 | Male | 3.5-4 | Smartphone | TRUE | Recreational | Urban | TRUE | TRUE | FALSE | FALSE
```

## 📊 Dashboard Components

### 1. **Population Overview** (Fixed Statistics)
- Baseline demographics for entire dataset
- Cross-demographic comparisons
- Population-wide benchmarks

### 2. **Filter Controls**
- Age Group selector
- Gender filter
- Residence Area filter

### 3. **Key Indicators** (Dynamic KPIs)
- Total Kids (filtered)
- Average Daily Screen Time
- Percentage Over Recommended Limit

### 4. **Usage Patterns**
- Device usage distribution
- Content type analysis
- Limit compliance by device/content

### 5. **Health Outcomes**
- Sleep, anxiety, obesity, and eye strain metrics
- Health correlations with screen time ranges
- Risk assessment by demographic segments

## 🎯 Key Insights Available

### Demographic Intelligence
- Screen time patterns across age groups
- Gender-based usage differences
- Urban vs rural digital habits
- Intersection analysis of multiple demographics

### Device & Content Strategy
- Primary device preferences by demographics
- Educational vs recreational content consumption
- Risk factors by device and content type

### Health Impact Assessment
- Direct correlations between screen time and health issues
- Risk thresholds identification
- Demographic-specific health patterns
- Early warning indicators

### Policy Applications
- Evidence-based screen time guidelines
- Targeted intervention strategies
- Resource allocation insights
- Digital wellness program effectiveness

## 🏥 Health Risk Analysis

The dashboard enables comprehensive health impact assessment:
- **Sleep Issues:** Correlation with screen time ranges
- **Eye Strain:** Device-specific risk patterns
- **Anxiety:** Mental health impact by demographics
- **Obesity:** Physical health correlation analysis

## 👥 Target Stakeholders

- **Parents & Educators:** Benchmark against population averages
- **Healthcare Professionals:** Identify at-risk populations
- **Policy Makers:** Design evidence-based digital wellness programs
- **Researchers:** Understand digital consumption patterns in Indian children

## 🚀 Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/indian-kids-screentime-dashboard.git
   ```

2. **Explore the data files:**
   - `original-data.xlsx` - Review the raw dataset
   - `clean-data.xlsx` - Examine the transformed data
   - `complete-analytics.xlsx` - View the full analysis including pivot tables and dashboard

3. **Review documentation:**
   - `project-overview.pdf` - Detailed project methodology and insights
   - `dashboard-images/` - Visual screenshots of the dashboard components

4. **Analyze the dashboard:**
   - Open `complete-analytics.xlsx` to interact with the live dashboard
   - Use the pivot tables to explore different data perspectives
   - Apply filters to analyze specific demographic segments

## 📈 Future Enhancements

- Time-series analysis for trend identification
- Machine learning models for risk prediction
- Geographic mapping for regional insights
- Integration with wearable device data

---

**Note:** This dashboard is designed to promote digital wellness among Indian children through data-driven insights and evidence-based interventions.
