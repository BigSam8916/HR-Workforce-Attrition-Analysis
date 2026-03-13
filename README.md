# HR Attrition Analysis — Executive Summary

**Analyst:** Samson Ogbonna | PostgreSQL · Power BI · SQL · Excel | Lagos, Nigeria

---

## 📊 Dataset Overview

| Item | Detail |
|---|---|
| **Total Employees** | 1,470 |
| **Total Variables** | 35 columns |
| **Tables Created** | 4 (employee, jobs, satisfaction, work_history) |
| **Schema Type** | Star Schema |
| **Data Quality** | ✅ No missing values detected |

---

## 🗄️ Database Architecture

```
emp_attrition (staging)
        │
        ├── employee       → demographics (age, gender, marital, education)
        ├── jobs           → compensation, role, department, attrition
        ├── satisfaction   → job satisfaction, WLB, environment
        └── work_history   → tenure, promotion, years in role
```

---

## 📋 SQL Queries & Business Questions Answered

| # | Business Question | Key Finding |
|---|---|---|
| 1 | How large is the workforce? | 1,470 unique employees, no duplicates |
| 2 | Any missing data? | ✅ Clean — no nulls in critical fields |
| 3 | Age distribution? | Peak concentration: ages 28–38 |
| 4 | Gender split? | ~60% Male · ~40% Female |
| 5 | Marital composition? | Married > Single > Divorced |
| 6 | Employees by department? | R&D largest · HR smallest |
| 7 | Employees by job role? | Sales Exec & Research Scientist highest headcount |
| 8 | Seniority pyramid? | Level 1 dominates — classic pyramid |
| 9 | Average salary by role? | Manager $17K · Sales Rep $2.6K (6.5× gap) |
| 10 | Overall attrition rate? | **16.1%** — 237 of 1,470 departed |
| 11 | Attrition by department? | Sales 20.6% · HR 19.0% · R&D 13.8% |
| 12 | Attrition by job role? | Sales Rep **39.8%** · Research Director 2.5% |
| 13 | Does overtime drive attrition? | OT Yes **30.5%** vs OT No **10.4%** (3× risk) |
| 14 | Does salary affect attrition? | Low income = highest attrition rate |
| 15 | Does job satisfaction matter? | Low satisfaction: 22.8% · High: 11.3% |
| 16 | Does gender influence attrition? | Males slightly higher — not primary driver |
| 17 | Does marital status matter? | Single **25.5%** · Married 12.5% · Divorced 10.1% |
| 18 | Does age affect attrition? | Young (<30) ranked #1 highest risk |
| 19 | Does work-life balance matter? | Bad WLB: **31.3%** · Good WLB: 14.2% |
| 20 | Do stock options reduce attrition? | Level 0: 24.4% · Level 1: **9.4%** (61% drop) |
| 21 | Does commute distance matter? | Far (>15mi): 20.7% · Near (≤5mi): 13.8% |
| 22 | Are newer employees at higher risk? | Year 0–2 spike: up to **36%** attrition |
| 23 | Does lack of promotion drive exits? | Yes — longer gaps = higher attrition |
| 24 | Does education affect attrition? | Mild effect — not a primary driver |
| 25 | Who is at imminent flight risk? | Employees with low pay + low satisfaction + OT + poor WLB |

---

## 🔍 Key Insights

### 1️⃣ Attrition is Above Industry Benchmark
> **16.1%** overall vs ~13% industry average — **1 in 6 employees has left**

### 2️⃣ Overtime is the #1 Single Predictor
> Overtime = **30.5%** attrition · No Overtime = **10.4%** → **3× multiplier**

### 3️⃣ Sales Representatives Are in Structural Crisis
> **39.8% attrition** · Earn only **$2,626/month** — lowest paid, highest pressured role

### 4️⃣ Low Pay Drives 65% of All Departures
> Leavers avg: **$4,787/month** · Stayers avg: **$6,833/month** → **$2,046 gap**

### 5️⃣ Youth + Single = Highest Risk Demographic
> Under 30: highest attrition rank · Single employees: **25.5%** departure rate

### 6️⃣ Stock Options = Best ROI Retention Tool
> Level 0 → Level 1 stock options cuts attrition from **24.4% to 9.4%** — a **61% reduction**

### 7️⃣ Poor Work-Life Balance Triggers Mass Exits
> Level 1 WLB: **31.3% attrition** — highest of any single satisfaction variable

### 8️⃣ The High-Risk Register is Actionable Now
> Query 25 surfaces employees at imminent risk by employee number and department

---

## ✅ Recommendations

| Priority | Action | Est. Impact |
|---|---|---|
| 🔴 **01 — Immediate** | Reform overtime policy — cap OT, add comp days | ~6pp drop for 416 OT staff |
| 🔴 **02 — High** | Pay review for Sales Rep, Lab Tech, HR, Research Scientist | Targets 65% of all attrition |
| 🔴 **03 — High** | Extend Level 1 stock options to 631 Level-0 employees | Retain ~95 employees/year |
| 🟡 **04 — Medium** | Structured 90-day onboarding with milestone check-ins | Fix 36% early-tenure spike |
| 🟡 **05 — Medium** | Quarterly pulse surveys (5 questions) | Catch risk 3–6 months early |
| 🟡 **06 — Medium** | Structured promotion cycles every 18 months | Reduce career-stagnation exits |
| 🟢 **07 — Low Cost** | Hybrid/remote policy for employees >15 miles from office | Close 6.9pp commute gap |

---

## 🎯 Conclusion

The **16.1% attrition rate is not random.** Three compounding root causes drive the majority of departures:

```
💰 Compensation Inequity   →  $2,046/month pay gap · 65% of exits in 4 roles
⏰ Operational Overload    →  Overtime triples attrition risk · affects 28% of workforce  
😞 Engagement Deficit      →  Low satisfaction & WLB are quantified, predictive risk variables
```

> The data is **actionable today.** Query 25 names the at-risk employees. The salary analysis identifies the exact roles. The overtime data flags who is at 3× departure risk.

**12-Month Target:**

```
Reduce attrition:   16.1%  →  below 12%
Retain additional:  60+ employees per cycle
Recover costs:      ~$307K in annual replacement savings
```

> *The cost of inaction compounds every quarter.
> The cost of intervention is a fraction of the talent loss already occurring.*

---
*Prepared by: **Samson Ogbonna** · Data Analyst · son.ogbonna@gmail.com · Lagos, Nigeria*
