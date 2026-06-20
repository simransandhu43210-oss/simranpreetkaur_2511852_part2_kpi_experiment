# Hypothesis Test Notes

## Metric Being Tested
Paid Conversion Rate
(Users who converted to paid / Total users in group)

## Reason for Choosing This Metric
Paid Conversion Rate is the North Star metric for this experiment.
It directly measures whether the new onboarding and activation 
campaign achieves its core business objective of converting 
free/trial users into paying customers.

## Null Hypothesis (H₀)
The paid conversion rate of the Treatment group is equal to 
or less than the Control group.
H₀: p_treatment ≤ p_control

## Alternate Hypothesis (H₁)
The paid conversion rate of the Treatment group is greater 
than the Control group.
H₁: p_treatment > p_control

## Test Type
One-tailed z-test for proportions

## Why One-Tailed
We only care if Treatment is BETTER than Control.
We are not interested in whether it is just different.
A one-tailed test is appropriate when the business question
is directional — "is the new campaign better?"

## Significance Level
α = 0.05 (5%)
This means we accept a 5% chance of wrongly rejecting H₀.

## Decision Rule
- If p-value < 0.05 → Reject H₀ → Treatment is significantly 
  better → Consider launching
- If p-value ≥ 0.05 → Fail to reject H₀ → Not enough evidence 
  → Do not launch

## Interpretation Logic
If we reject H₀, it means the improvement in paid conversion 
rate seen in the Treatment group is statistically significant 
and not due to random chance. However, we must also check 
guardrail metrics (refund rate, support ticket rate, revenue 
per converted user) before making the final launch decision.

## Connection to Business Decision
The hypothesis test result directly informs whether leadership 
should launch the new campaign to all users. A statistically 
significant result in the primary metric, combined with 
acceptable guardrail metrics, would support a full launch 
recommendation.

## Test Results

| Input | Value |
|---|---|
| Control Users | 693 |
| Treatment Users | 715 |
| Control Conversions | 22 |
| Treatment Conversions | 50 |
| Control Conversion Rate | 3.17% |
| Treatment Conversion Rate | 6.99% |
| Z-Statistic | 3.252 |
| P-Value (one-tailed) | 0.000573 |
| Significant at α=0.05 | YES |

## Decision
P-value (0.000573) < α (0.05) → Reject H₀

## Business Interpretation
The Treatment campaign produces a statistically significant
improvement in paid conversion rate. The probability of this
result occurring by chance is less than 0.06%. This is strong
evidence that the new campaign genuinely improves conversion.

However, guardrail metrics must be checked before final
launch decision — particularly support ticket rate (+10%)
and revenue per converted user (-$859).

## Guardrail Metrics Evaluation

### Guardrail 1: Refund Rate
| | Control | Treatment |
|---|---|---|
| Refund Rate | 0.00% | 0.42% |

**Risk Assessment: MEDIUM RISK ⚠️**
The Treatment group has a small but non-zero refund rate
while Control has none. This means some users who converted
under the new campaign immediately requested refunds.
This could indicate the campaign is creating false
expectations about the product.

### Guardrail 2: Support Ticket Rate
| | Control | Treatment |
|---|---|---|
| Support Ticket Rate | 14.72% | 24.76% |

**Risk Assessment: HIGH RISK 🔴**
Support ticket rate increased by 10 percentage points in
the Treatment group. This is the most concerning guardrail
finding. Nearly 1 in 4 Treatment users raised a support
ticket compared to 1 in 7 Control users. This signals
the new campaign may be causing confusion, unmet
expectations, or product dissatisfaction.

### Guardrail 3: Revenue Per Converted User
| | Control | Treatment |
|---|---|---|
| Revenue Per Converted User | $1,630.10 | $770.41 |

**Risk Assessment: HIGH RISK 🔴**
Although Treatment converts more users, each converted
user generates 53% less revenue than Control converted
users. This suggests the campaign may be attracting
lower-value customers or users on cheaper plans.
Higher conversion volume does not guarantee higher
total revenue if revenue per user drops significantly.

### Overall Guardrail Conclusion
Two out of three guardrail metrics show HIGH RISK.
Despite the statistically significant improvement in
paid conversion rate, the guardrail findings suggest
a full immediate launch carries meaningful business risk.
A selective or phased launch is recommended over
full immediate rollout.
