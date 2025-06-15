
<p align="center">
  <img src="https://github.com/user-attachments/assets/fb4f7462-a8bf-4aa2-abec-ef2704b1319e" alt="ab_testing_image" width="700"/>
</p>


# A/B Testing: Search Ranking Algorithm Impact on Booking Conversion

This project analyzes the results of an A/B test conducted by a leading online travel agency to evaluate a new search ranking algorithm. The objective is to determine whether the new algorithm improves user conversion rates without negatively affecting the booking experience.

---

## Problem Statement

The Product team deployed a new search ranking system aimed at improving the booking conversion rate. Before full rollout, they require:

- Statistically significant **increase in conversion rate** (primary metric)
- **No significant increase** in **time to booking** (guardrail metric)

---

## Datasets

- `sessions_data.csv`: Session-level logs with timestamps, bookings, and time to booking.
- `users_data.csv`: User-level experiment group assignment (control or variant).

---

## Metrics Analyzed

| Metric           | Type       | Goal                              | Test Used            |
|------------------|------------|------------------------------------|-----------------------|
| Conversion Rate  | Binary (0/1)| Increase                          | Z-test for proportions |
| Time to Booking  | Continuous | Should not increase               | Two-sample t-test      |

Effect sizes were also calculated to assess business impact beyond p-values.

---

## Statistical Approach

- Confidence level: **90%** (α = 0.10)
- ✅ Z-test for conversion rate (one-sided: variant > control)
- ✅ T-test for time to booking (two-sided)
- ✅ SRM (Sample Ratio Mismatch) check using chi-square test
- ✅ Relative effect size estimation

---

## Results Summary

- **Conversion Rate**: Variant group showed a statistically significant improvement.
- **Time to Booking**: No significant difference; variant group was slightly faster.
- ✅ **Recommendation**: Proceed with full rollout.

---

## Key Takeaways

- Applied real-world A/B testing design and analysis techniques.
- Validated experiment randomization using chi-square SRM check.
- Measured both statistical and practical (effect size) significance.
- Demonstrated guardrail metric monitoring to protect user experience.

---

## Tools & Libraries

- Python (Pandas, NumPy)
- `scipy.stats` (t-test, z-test)
- `statsmodels` (proportions testing)
- `matplotlib` / `seaborn` (EDA visualizations)

---

