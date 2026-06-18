# Error Analysis

## False Positives

- **CUST01246**: predicted 98.5% churn but did not churn. Signals: recency 262, sessions 1, tickets 0, monetary INR 0. Interpretation: model may overreact to inactivity/support risk when latent intent remains.
- **CUST01864**: predicted 97.6% churn but did not churn. Signals: recency 221, sessions 3, tickets 0, monetary INR 0. Interpretation: model may overreact to inactivity/support risk when latent intent remains.
- **CUST01325**: predicted 96.3% churn but did not churn. Signals: recency 186, sessions 1, tickets 0, monetary INR 0. Interpretation: model may overreact to inactivity/support risk when latent intent remains.
- **CUST02313**: predicted 95.1% churn but did not churn. Signals: recency 171, sessions 3, tickets 0, monetary INR 583. Interpretation: model may overreact to inactivity/support risk when latent intent remains.
- **CUST01411**: predicted 94.6% churn but did not churn. Signals: recency 183, sessions 0, tickets 0, monetary INR 0. Interpretation: model may overreact to inactivity/support risk when latent intent remains.

## False Negatives

- **CUST02072**: predicted 5.2% churn and actually churned. Signals: recency 35, sessions 4, tickets 0, monetary INR 4,340. Interpretation: customer looked safer than outcome; monitor weak signals such as category fatigue or consent/channel mismatch.
- **CUST01700**: predicted 7.1% churn and actually churned. Signals: recency 6, sessions 14, tickets 0, monetary INR 2,045. Interpretation: customer looked safer than outcome; monitor weak signals such as category fatigue or consent/channel mismatch.
- **CUST00184**: predicted 7.4% churn and actually churned. Signals: recency 14, sessions 6, tickets 0, monetary INR 2,457. Interpretation: customer looked safer than outcome; monitor weak signals such as category fatigue or consent/channel mismatch.
- **CUST00727**: predicted 7.9% churn and actually churned. Signals: recency 8, sessions 10, tickets 0, monetary INR 2,696. Interpretation: customer looked safer than outcome; monitor weak signals such as category fatigue or consent/channel mismatch.
- **CUST02096**: predicted 8.6% churn and actually churned. Signals: recency 5, sessions 9, tickets 0, monetary INR 1,425. Interpretation: customer looked safer than outcome; monitor weak signals such as category fatigue or consent/channel mismatch.
