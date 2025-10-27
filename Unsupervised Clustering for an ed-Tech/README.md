# 🧠 Decoding The Talents And The Needs
### An Unsupervised Case Study for Learner Profiling & Company Profiling for Scaler

---

##  Project Overview
Scaler, an emerging tech-versity, aims to deliver world-class education in computer science and data science. However, with learners from diverse professional backgrounds, understanding their current roles, companies, and experiences becomes crucial. This project applies **unsupervised learning techniques** to profile learners and companies, enabling Scaler to:

- Deliver personalized and relevant learning experiences.
- Tailor content recommendations and mentorship programs.
- Identify and profile top companies and job positions for alumni.

---

## 🎯 Business Challenge
The challenge lies in **identifying patterns within a diverse learner database** — job roles, employers, and experience levels — to group similar learners together. These clusters can then inform strategic educational and operational decisions.

---

## 🎯 Objectives
1. **Cluster learners** based on their professional attributes such as job role, company, and experience.
2. **Evaluate cluster quality** using quantitative metrics and domain relevance.
3. **Generate actionable insights** for personalized learning paths, targeted mentorship, and job profiling.
4. **Provide recommendations** for Scaler’s data-driven learner engagement and content strategies.

---

## 🧩 Scope of Work
1. **Data Understanding & Preprocessing**
   - Performed likes of Univariate and Bivariate Analysis for EDA, handled missing values, and prepare data for clustering.
   - Identify and remove outliers, irrelevant data points, and noise.

2. **Feature Engineering**
   - Create derived variables such as **Years of Experience (YOE)** and **Promotion Status**.
   - Standardize job titles for consistency (e.g., “SDE 1” → “Software Engineer 1”).

3. **Clustering Techniques**
   - Implement algorithms such as **K-Means** and **Hierarchical Clustering**.
   - Use **Elbow Method** and **Dendrogram Analysis** to determine optimal cluster count.

4. **Cluster Evaluation**
   - Applied **Silhouette Score**, **Davies-Bouldin Index**, and **intra/inter-cluster analysis** for quantitative evaluation.
   - And PCA,Tsne and UMAP for Qualitative Evaluation for respective algorithms.

5. **Insights & Recommendations**
   - Derive meaningful insights for curriculum design, mentorship allocation, and company engagement.

---

## ⚙️ Project Workflow Summary

| Step | Description |
|------|--------------|
| **Data Cleaning** | Started with 205,843 rows. Imputed missing job positions (kNN/Mode) and dropped missing company data. |
| **Standardization** | Normalized inconsistent job titles to improve clustering quality. |
| **Feature Creation** | Added YOE and Promotion Status (though <5% promoted recently). |
| **Segmentation (Business Logic)** | Created rule-based groups (Top/Bottom 10 earners per company/job). |
| **Encoding** | Used Frequency Encoding for `company_hash` (32k+) and Label Encoding for `job_position` (452 unique). |
| **Clustering** | Both K-Means and Hierarchical Clustering indicated **4 optimal clusters**. |

---

## 📊 Key Segmentation Approaches

### **Approach 1: Business Logic-Based Segmentation**
- **Tier 1 / Tier 3:** Top and bottom 10 earners per company.
- **Class 1 / Class 3:** Top and bottom 10 earners per job position within a company.
- **Tier X:** Top earners with specific YOE in specific role/company.

### **Approach 2: Unsupervised ML Clustering**
- **Algorithm:** K-Means and Hierarchical Clustering.
- **Optimal Clusters:** 4 (determined via Elbow Method).
- **Feature Encoding:** Hybrid of frequency and label encoding for high-cardinality categorical data.

---

## 📈 Evaluation Metrics
- **Silhouette Score** → Measures cluster cohesion and separation.
- **Davies-Bouldin Index** → Lower values indicate better clustering.
- **Domain Validation** → Ensured clusters made logical business sense.
- **Hopkins statistics** → To make sure data is clusterable or not
---

## 🔍 Insights & Business Impact
- Identified key learner segments based on **experience, company type, and compensation**.
- Helped Scaler design **targeted mentorship programs** for high-performing clusters.
- Enabled **personalized content delivery** to enhance learning efficiency.
- Provided **company profiling insights** to align alumni placement and partnerships.

---

## 🧰 Tech Stack
| Category | Tools / Libraries |
|-----------|-------------------|
| **Programming Language** | Python 3.12 |
| **Libraries** | pandas, numpy, sklearn, scipy |
| **Visualization** |matplotlib / seaborn / Plotly |
| **Dimensionality Reduction** | PCA, Tsne, UMAP |
| **Modeling** | K-Means, Hierarchical Clustering |

---
