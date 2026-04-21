# 🎬 Netflix Case Study — Exploratory Data Analysis

> **Tools Used:** Python | Pandas | NumPy | Matplotlib | Seaborn
> **Dataset:** 100 Users | 43 Unique Shows | 10 Genres | 3 Subscription Types

---

## 📌 Objective

Analyze Netflix user behavior data to uncover viewing patterns, subscription value, genre engagement, and user segmentation using Python — supporting data-driven content and pricing decisions.

---

## 🗃️ Dataset Structure

| Column | Type | Description |
|--------|------|-------------|
| `user_name` | object | Name of the user |
| `show_name` | object | Name of the show watched |
| `genre` | object | Genre of the show |
| `episodes_watched` | int64 | Number of episodes watched |
| `rating_given` | float64 | User rating (out of 5) |
| `hours_watched` | float64 | Total hours watched |
| `subscription_type` | object | Basic / Standard / Premium |

---

## 🔍 Key Insights

| Metric | Value |
|--------|-------|
| 👥 Total Users | 100 |
| 🎭 Unique Shows | 43 |
| 🎬 Unique Genres | 10 |
| 📺 Most Watched Show | The Good Place (6 users) |
| 👤 Most Active User | Lily (watching 4 shows) |
| ⭐ Avg Rating | 3.7 / 5.0 |
| 📊 Avg Episodes Watched | 41 episodes |
| ⏱️ Avg Hours Watched | 32 hours |
| 💳 Most Popular Subscription | Standard (39 users) |
| 🎭 Most Popular Genre | Romance (14 users) |
| 🔁 No Duplicates or Nulls | ✅ Clean Dataset |

---

## 📊 Subscription Analysis

| Subscription | Price (₹) | Avg Hour Price | Avg Value Score |
|---|---|---|---|
| Basic | ₹149 | ₹7.3/hr | 124 |
| Standard | ₹199 | ₹10.5/hr | 169 |
| Premium | ₹499 | ₹43.3/hr | 163 |

> **Insight:** Premium users pay the most but watch the least — lowest value for money. Standard offers the best value score.

---

## 👥 User Segmentation

| Category | Count | Avg Episodes |
|---|---|---|
| Experienced (≥10 episodes) | 91 | 44.8 |
| New (<10 episodes) | 9 | 6.1 |

---

## 🎭 Genre Engagement Labels

| Condition | Label |
|---|---|
| Genre = Drama AND rating ≥ 4.0 | Drama Fan |
| Genre = Comedy AND rating ≥ 4.0 | Comedy Fan |
| rating < 3.0 | Not Engaged |
| All other cases | Neutral Viewer |

> 18 users were watching more than 1 genre

---

## 🛠️ Python Concepts Used

- `pandas` — data loading, cleaning, groupby, aggregations
- `map()` — mapping subscription types to prices
- `apply()` — custom functions for feature engineering
- `groupby()` — segmentation and aggregation analysis
- `isna() / duplicated()` — data quality checks
- **Feature Engineering** — created 6 new columns:
  - `subscription_price` — price mapped from subscription type
  - `hour_price` — cost per hour watched
  - `users_category` — New vs Experienced
  - `value_score` — (rating × hours) / price
  - `subscription_weight` — weighted score by plan
  - `genre_engagement` — Drama Fan / Comedy Fan / Not Engaged / Neutral Viewer

---

## 📁 Files in this Repository

| File | Description |
|------|-------------|
| `Netflix_case_study.ipynb` | Full Jupyter Notebook with analysis |
| `README.md` | Project documentation |

---

## ▶️ How to Run

1. Clone this repository
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```
3. Open `Netflix_case_study.ipynb` in Jupyter Notebook or Google Colab
4. Run all cells from top to bottom

---

## 👤 Author

**Senapathi Krishna Sai**
Data Analyst | SQL | Python | Tableau | Excel

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/senapathi-krishna-sai-a54721388)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/senapathi402-star)
