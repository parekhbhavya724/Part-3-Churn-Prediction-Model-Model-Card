# Model Card

## Intended Use

Predict whether a D2C customer is likely to churn in the 60 days after the 2025-09-30 snapshot so retention teams can prioritize outreach.

## Data

The model uses `rfm_modeling_snapshot.csv`, which the data dictionary states is built only from information available on or before 2025-09-30. The target is `churn_next_60d`; `customer_id`, `snapshot_date`, `split`, and the target are excluded from features.

## Model And Performance

Selected model: `baseline_logistic_regression`. Business threshold: `0.2`.

Validation: {"threshold": 0.2, "accuracy": 0.6994, "precision": 0.5991, "recall": 0.9456, "f1": 0.7335, "roc_auc": 0.8826, "pr_auc": 0.8676, "confusion_matrix": [[96, 93], [8, 139]]}

Test: {"threshold": 0.2, "accuracy": 0.6845, "precision": 0.6183, "recall": 0.9643, "f1": 0.7535, "roc_auc": 0.885, "pr_auc": 0.8784, "confusion_matrix": [[68, 100], [6, 162]]}

Baseline validation: {"threshold": 0.5, "accuracy": 0.8155, "precision": 0.7972, "recall": 0.7755, "f1": 0.7862, "roc_auc": 0.8826, "pr_auc": 0.8676, "confusion_matrix": [[160, 29], [33, 114]]}

## Top Drivers

| feature                           |   importance |
|:----------------------------------|-------------:|
| num__recency_days                 |     1.74402  |
| num__monetary_180d                |     0.440689 |
| cat__preferred_category_Fragrance |     0.384134 |
| cat__acquisition_channel_Organic  |     0.378022 |
| num__return_rate_180d             |     0.341913 |
| cat__loyalty_tier_Platinum        |     0.315393 |
| num__ticket_count_90d             |     0.301747 |
| num__negative_ticket_rate_90d     |     0.300531 |
| num__last_visit_days_ago          |     0.293952 |
| num__avg_discount_pct_180d        |     0.290645 |
| cat__preferred_category_Baby Care |     0.282206 |
| num__sessions_30d                 |     0.204736 |
| cat__preferred_category_Skin Care |     0.190011 |
| num__campaign_clicks_30d          |     0.177054 |
| num__frequency_180d               |     0.168884 |

## Limitations

The labels measure no purchase in the next 60 days, not customer dissatisfaction. Some customers may be seasonal or temporarily inactive. The model should not be used as the only reason for denying service, changing prices, or making sensitive inferences.

## Ethical And Responsible Use

Use the score to prioritize helpful retention actions, not to pressure customers or over-discount vulnerable groups. Respect marketing consent and channel preferences.

## Monitoring

Track feature drift, score distribution, precision/recall on later cohorts, campaign holdout lift, complaint rates, opt-outs, and retraining triggers after changes in pricing, logistics, campaigns, or product mix.
