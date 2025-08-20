

# ⚽ Investigating Goal Scoring in Men's vs. Women's FIFA World Cups

## 📖 Project Overview

As a sports journalist specializing in soccer analysis, I’ve long had the gut instinct that **more goals are scored in women’s international soccer matches than men’s**. But instincts need evidence.

This project investigates whether that belief holds up statistically, using official match results from **FIFA World Cup tournaments (excluding qualifiers) since January 1, 2002**.

By applying statistical hypothesis testing, we seek to answer a single core question:

> **Are more goals scored in women’s international soccer matches than men’s?**

---

## 🎯 Hypotheses

We test this research question using a **one-tailed hypothesis test** at a **10% significance level (α = 0.10)**:

* **Null Hypothesis (\$H\_0\$):**
  The mean number of goals scored in women’s FIFA World Cup matches is the same as men’s.

* **Alternative Hypothesis (\$H\_A\$):**
  The mean number of goals scored in women’s FIFA World Cup matches is **greater than men’s**.

---

## 📂 Data Sources

Two datasets were used, both scraped from a reliable online source of historical international soccer results:

* `women_results.csv` → Official women’s international match results since the 19th century.
* `men_results.csv` → Official men’s international match results since the 19th century.

Both datasets include:

* Date of match
* Competing teams
* Goals scored by each team
* Tournament type

For this project, only **FIFA World Cup matches since 2002** are included.

---

## 🛠️ Methodology

1. **Data Cleaning & Filtering**

   * Select only FIFA World Cup matches.
   * Exclude qualifiers.
   * Restrict data to matches played after `2002-01-01`.

2. **Feature Engineering**

   * Compute **total goals per match** (sum of goals scored by both teams).

3. **Statistical Analysis**

   * Perform a **two-sample t-test** (Welch’s t-test, unequal variances).
   * One-tailed test, significance level α = 0.10.

4. **Interpretation**

   * If *p-value < 0.10*: reject \$H\_0\$ → conclude that women’s matches have significantly more goals.
   * If *p-value ≥ 0.10*: fail to reject \$H\_0\$ → conclude that evidence is insufficient.

---

## 📊 Expected Outcome

* A clear statistical answer to whether **women’s international soccer matches produce more goals than men’s**.
* Insight into how styles of play, competition levels, and match dynamics differ between men’s and women’s FIFA World Cups.

---

## 🚀 How to Run the Analysis

1. Clone this repository:

   ```bash
   git clone https://github.com/your-username/fifa-goals-analysis.git
   cd fifa-goals-analysis
   ```
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter Notebook:

   ```bash
   jupyter notebook analysis.ipynb
   ```

---

## 📌 Significance of the Study

This analysis blends **sports journalism and statistical science** to answer a question that fans, analysts, and researchers have debated for years.

By grounding observations in data rather than gut feeling, we contribute to a more nuanced understanding of how the men’s and women’s games compare on the world’s biggest stage.

---

