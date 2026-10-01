# 🛒 E-Commerce Checkout A/B Testing & Revenue Optimization

An end-to-end e-commerce experimentation project evaluating the business impact of a **One-Click Instant Checkout** feature (Variant B) against the traditional checkout flow (Control A) on 2,489 unique user journeys using **Advanced Excel** and **Statistical Hypothesis Testing**.

---

## 📌 Executive Summary & Key Results
* **Primary Metric (Conversion Rate):** Increased from **12.96%** (Control A) to **16.56%** (Variant B), delivering an absolute lift of **+3.60% points** (+27.77% relative lift).
* **Statistical Rigor (Two-Sample Z-Test):** Calculated **Z-score = 2.53** and **P-value = 0.011** ($p < 0.05$), confirming statistical significance at a **98.8% confidence level**.
* **Guardrail Metric (AOV):** Maintained stable Average Order Value (**₹2,705.65 vs ₹2,648.18**), ensuring zero revenue cannibalization.
* **Business Recommendation:** **100% Production Rollout** across all customer cohorts.

---

## 💼 Business Problem & Context
The e-commerce platform experienced drop-offs during the final checkout stage. The product team proposed an expedited **"One-Click Checkout"** experience to reduce cart abandonment. 

As a Data Analyst, the goal was to:
1. Validate whether the new checkout variant drives statistically significant conversion gains.
2. Monitor guardrail metrics (Average Order Value) to ensure faster checkout doesn't reduce basket size.
3. Investigate heterogeneous treatment effects across customer segments (New, Returning, VIP).

---

## 🛠️ Tools & Analytical Techniques
* **Analytics Tool:** Microsoft Excel (Data Cleaning, Pivot Tables, Calculated Fields, Executive Dashboard)
* **Statistical Methods:** Two-Sample Z-Test for Proportions, Pooled Variance, Standard Error, P-Value Benchmarking ($\alpha = 0.05$)
* **Data Concepts:** Simpson's Paradox Protection, Cohort Segmentation, Guardrail Metric Monitoring

---

## 🔬 Experimentation & Statistical Methodology

### 1. Data Audit & Preprocessing
* Removed duplicate transaction logs ensuring single-user journey integrity.
* Standardized inconsistent categorical tags (`clean_test_group`, `clean_device`).
* Filtered negative/invalid values in page views and transactional amounts.

### 2. Hypothesis Testing Framework
* **Null Hypothesis ($H_0$):** $CR_B - CR_A = 0$ (No difference between control and variant).
* **Alternative Hypothesis ($H_1$):** $CR_B - CR_A \neq 0$ (Variant B significantly impacts conversion).

$$\text{Pooled Probability } (p) = \frac{X_A + X_B}{N_A + N_B} = \frac{159 + 209}{1,227 + 1,262} = 14.79\%$$

$$\text{Standard Error } (SE) = \sqrt{p(1-p)\left(\frac{1}{N_A} + \frac{1}{N_B}\right)} = 1.42\%$$

$$Z\text{-Score} = \frac{CR_B - CR_A}{SE} = \frac{16.56\% - 12.96\%}{1.42\%} = \mathbf{2.53}$$

$$\text{P-Value} = \mathbf{0.011} \quad (p < 0.05 \implies \text{Reject } H_0)$$

---

## 📊 Segment Performance Deep-Dive

To protect against Simpson's Paradox, performance was segmented across user tiers:

| Customer Segment | Control A (CR) | Variant B (CR) | Absolute Lift | Cohort Impact |
| :--- | :---: | :---: | :---: | :--- |
| **New Users** | 10.56% | 13.53% | **+2.97%** | Reduced initial onboarding friction |
| **Returning Users** | 12.04% | 16.17% | **+4.13%** | Re-engaged drop-off shoppers |
| **VIP Users** | 23.53% | 28.80% | **+5.27%** | Accelerated high-value purchase flow |

---

## 📈 Executive Dashboard Features
* **Dynamic KPI Scorecards:** Real-time visibility into traffic volume, baseline rates, variant conversion, and statistical significance.
* **Segment Clustered Bar Visuals:** Side-by-side performance validation preventing cohort cannibalization.
* **Interactive Slicers:** Dynamic filtering by device type and customer cohorts.

---

## 🚀 Business Recommendation & Next Steps
1. **Full Rollout:** Deploy One-Click Checkout to 100% of e-commerce traffic.
2. **Post-Launch Guardrail Tracking:** Monitor 30-day return rates and order cancellation rates to ensure instant checkout does not cause accidental purchases.
