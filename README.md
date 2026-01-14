# 📺 OTT Viewer Retention & Episode Performance Analysis
### A Strategic Tableau Dashboard Analyzing 33,000+ Episodes Across 487 Shows

![Dashboard Preview](files/ott_viewership.gif
)  


**>Interactive Dashboard**: [View on Tableau Public](https://public.tableau.com/views/OTTViewershipDashboard/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

---

## 📌 Executive Summary

This dashboard answers **18 strategic business questions** about why viewers abandon TV shows mid-season and which episodes face the highest churn risk.

**The Core Finding:** Cognitive load (content complexity) is a **bigger churn driver than narrative hooks**—a counterintuitive insight that directly informs content strategy.

---

## 🎯 The Problem

**Why This Matters:**
Streaming platforms lose billions in subscriber lifetime value due to mid-season viewer drop-off. Understanding *why* and *when* viewers leave is critical for content investment decisions.

**What I Investigated:**
- Do strong narrative hooks guarantee viewer retention?
- Which content characteristics drive engagement vs. abandonment?
- How do genre, platform, and episode position interact to affect churn?
- Can we identify episodes that need immediate intervention?

**Dataset:** 33,171 episodes | 487 unique shows | 16 genres | 28 platforms | Kaggle Open Source

---

## 💡 Key Insights (What Executives Need to Know)

### 🔴 1. Cognitive Load is the Hidden Churn Driver
**Finding:** Episodes with high cognitive load (complexity >7.5) see **40% higher drop-off** than simpler ones.
- **Implication:** Content redesign focus should prioritize simplifying complex narratives, not adding more "hooks."
- **Action:** Flag high-complexity episodes in Drama and Sci-Fi; recommend narrative simplification or targeted marketing.

### 🟢 2. Genre Matters More Than Platform
**Finding:** Comedy retains viewers at **64% completion**, while Drama lags at **52%**—a **23% performance gap** that holds *across all platforms*.
- **Question for Strategists:** What's Comedy's secret? (Lower cognitive load, faster pacing, episodic structure?)
- **Implication:** Platform customization is less important than genre-specific narrative design.

### 🟡 3. Mid-Season Fatigue is Real and Measurable
**Finding:** Episodes 11-50 experience an **8-12% engagement dip** compared to Pilots and Finales.
- **Implication:** Season arcs must maintain momentum through the middle third; this is where shows are cancelled.
- **Action:** Increase production quality/hooks for episodes 15-25; front-load plot revelations earlier.

### 🔵 4. Identify and Intervene on At-Risk Episodes
**Finding:** **6% of content** (~2,000 episodes) shows drop-off probability >0.65—a manageable intervention pool.
- **Action Items:**
  - Marketing push on high drop-off + low hook-strength episodes
  - Rescheduling risky episodes away from competing content
  - Re-editing or re-promoting episodes with poor engagement signals

### ⚫ 5. Platform Customization Matters (Conditionally)
**Finding:** Drama performs differently on each platform (HBO Max vs. Netflix vs. Hulu), suggesting **audience composition** and **marketing strategy** vary by platform.
- **Implication:** A one-size-fits-all content strategy fails. Platform-specific tuning is required.

---

## 🏗️ Dashboard Architecture: Answering 18 Strategic Questions

I didn't just build charts—I built a **decision-making framework** with 18 interlocking questions:

### **Step 1: Baseline Metrics (Q1-3)** → KPI Cards
- Overall engagement landscape (Avg Watch %, drop-off distribution, risk percentages)
- Variance by genre and platform
- Macro trends in retention risk

### **Step 2: Content Quality Drivers (Q4-6)** → Analytical Charts
- Q4: What predicts higher completion? → Hook strength analysis
- Q5: Does episode position matter? → Episode position trend line
- Q6: Is cognitive load a deal-breaker? → Complexity vs. engagement correlation

### **Step 3: Risk Segmentation (Q7-9)** → Heatmaps & Risk Breakdown
- Q7: Which episodes should be flagged? → Risk category distribution
- Q8: What genre-platform combos fail? → Genre × Platform heatmap
- Q9: Does show age affect retention? → Show maturity analysis

### **Step 4-6: Actionable Insights** → Word Cloud + Interactive Filters
- Identify the **most vulnerable shows** by name (Word Cloud)
- Drill from macro (all content) to micro (specific at-risk episodes) using cross-filtering
- Enable stakeholders to ask their own "what-if" questions

---

## 🛠️ Technical Execution: Advanced Tableau Features

**This dashboard demonstrates:**

### Calculated Fields (10 Custom Metrics)
- **Engagement Quality Score:** Weighted composite (40% completion + 30% anti-drop-off + 30% hook strength)
  - *Why?* Predicts retention better than any single metric.
- **Content Complexity Index:** Aggregates cognitive load, dialogue density, visual intensity.
  - *Why?* Reveals the "complexity penalty" on viewer behavior.
- **Risk Category:** IF/THEN logic to classify episodes (High Dropout, Low Engagement, Healthy).
- **Episode Position Category:** Groups episodes by narrative stage (Pilot, Early, Mid, Late, Legacy).
- **Show Maturity:** Categorizes shows by longevity (New, Growing, Established, Legacy).

### Multi-Dimensional Analysis
- **Heatmaps:** 16 genres × 5+ platforms; color-coded by drop-off probability.
- **Dual-Axis Charts:** Correlate engagement metrics with complexity trends.
- **Interactive Filters:** Genre, Platform, Risk Category, Show Maturity cross-filter all views.
- **Cross-Sheet Filtering:** Selecting a genre in one chart updates all dependent visualizations.

### Dashboard Interactivity
- **4 Strategic Filters:** Allow stakeholders to drill from executive summary to operational details.
- **Reset Button:** Custom dashboard action to clear all filters in one click.
- **Tooltips:** Rich context (show name, episode title, exact metrics) on hover.
- **Fixed Dashboard Size:** Consistent layout across devices and screen sizes.

---

## 📊 Visualizations (6 Strategic Views)

| # | Chart Type | Question Answered | Key Insight |
|---|-----------|------------------|-----------|
| 1 | **KPI Cards (6)** | Overall engagement health | 57% avg completion, 6% high-risk episodes |
| 2 | **Heatmap** | Genre × Platform performance | Drama struggles on all platforms; Comedy consistent |
| 3 | **Bar Chart** | Genre drop-off ranking | Comedy #1 (0.42), Drama worst (0.51) |
| 4 | **Line Chart** | Episode position impact | Mid-season dip visible; recovery at finales |
| 5 | **Risk Donut** | Risk category distribution | 85% healthy, 14% high-risk, 1% low-engagement |
| 6 | **Word Cloud** | Most vulnerable shows | Identify shows needing intervention by name |

---

## 🚀 How to Use This Dashboard

### **For Executives:**
> "Which genres/platforms are underperforming?"  
> *Filter by Genre → look at the Heatmap.*

### **For Content Strategists:**
> "Which specific episodes need marketing intervention?"  
> *Filter by Risk Category = "High Dropout" → reference Word Cloud for show names.*

### **For Data Teams:**
> "How does cognitive load affect churn?"  
> *Look at the correlation in the Complexity vs. Engagement analysis.*

### **For Recruiters/Hiring Managers:**
> "Show me your analytical thinking."  
> *Look at how 18 questions→6 visualizations creates a coherent story.*

---

## 💾 How to Access

### Option 1: Interactive Online
👉 **[View Live on Tableau Public](https://public.tableau.com/views/OTTViewershipDashboard/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link))
- Interact with filters
- Hover for details
- Explore the data yourself

### Option 2: Download & Explore Locally
1. Clone this repository
2. Download ![OTT Viewership Dashboard.twbx](files/OTT_Viewership_Dashboard.twbx)
4. Open in Tableau Desktop
5. Inspect calculated fields, filter logic, and design

### Option 3: View Static Dashboard
- Screenshot included as `Dashboard.png`

---

## 🧠 What I Learned (Technical + Strategic)

### **Tableau Skills Gained:**
- ✅ Calculated fields for composite metrics
- ✅ Multi-dimensional filtering and cross-sheet actions
- ✅ Color coding and design for stakeholder communication
- ✅ Handling imbalanced categorical data (risk categories)
- ✅ Dashboard performance optimization (33K rows)

### **Analytical Thinking:**
- ✅ Decompose a complex problem into 18 specific questions
- ✅ Prioritize insights by business impact, not visual appeal
- ✅ Use data to challenge assumptions (complexity > hooks)
- ✅ Create actionable recommendations, not just observations

### **Business Communication:**
- ✅ Design for the audience (KPIs for executives, drill-down for analysts)
- ✅ Highlight counterintuitive findings (they drive decisions)
- ✅ Frame insights as actions ("Flag high-complexity episodes" vs. "Complexity correlates with churn")

---

## 🎓 Key Takeaways for Portfolio Reviewers

**What This Project Demonstrates:**

1. **Strategic Thinking:** 18 questions → 6 visualizations → cohesive story (not just dashboards)
2. **Technical Competency:** Calculated fields, filtering, cross-sheet actions, professional design
3. **Business Acumen:** Insights are actionable; every chart drives a decision
4. **Scalability:** Works for 33K records; could handle production OTT data
5. **Communication:** Clear narrative, professional presentation, specific recommendations

**Why Hiring Managers Should Care:**
- This is what *real* analytics looks like: problem → decomposition → data → insights → action
- The candidate can think like a strategist AND execute with tools
- Portfolio-ready quality and documentation

---

## 📈 Metrics at a Glance

| Metric | Value | Insight |
|--------|-------|---------|
| Avg Watch Completion | 57% | Baseline engagement |
| High-Risk Episodes | 6% (2,033) | Manageable intervention pool |
| Best Genre (Completion) | Comedy @ 64% | 23% ahead of Drama |
| Worst Genre | Drama @ 52% | Needs strategic redesign |
| Cognitive Load Correlation | -0.69 | Strong negative: complexity kills engagement |
| Mid-Season Dip | 8-12% | Episodes 11-50 are danger zone |
| Shows Analyzed | 487 | Across 28 platforms |

---

## 🔗 Links & Resources

- **Dashboard Link:** [Tableau Public](https://public.tableau.com/views/OTTViewershipDashboard/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
- **Data Source:** [Kaggle OTT Dataset](https://www.kaggle.com/datasets/eklavya16/ott-viewer-drop-off-and-retention-risk-dataset)
- **My LinkedIn:** [Connect](https://www.linkedin.com/in/abhinav-d-b713b2214/)
- **Portfolio:** [GitHub](https://github.com/dubeyabhinav/OTT-Viewership-Retention/)

---

## 📄 Files in This Repository

```
OTT-Viewer-Retention-Dashboard/
├── README.md (this file)
├── Ott_Viewer_Retention.twbx (Tableau workbook)
├── Dashboard_Screenshot.png (high-res image)
├── Dashboard_Demo.mp4 (optional: screen recording)
└── Data/
    └── ott_viewer_retention_data.csv (Kaggle source, if included)
```

---

## 🙏 Acknowledgments

- **Data Source:** Kaggle - OTT Viewer Drop-off & Retention Risk Dataset
- **Tool:** Tableau Public
- **Inspiration:** Real streaming platform analytics challenges

---

**Questions or feedback?** Feel free to open an issue or reach out directly.

**Interested in collaborating on analytics projects?** Let's connect! 🚀

---

*Last Updated: December 26, 2025*

*Author: [Abhinav Dubey](https://www.linkedin.com/in/abhinav-d-b713b2214/) | Data Analyst | Portfolio Project*

