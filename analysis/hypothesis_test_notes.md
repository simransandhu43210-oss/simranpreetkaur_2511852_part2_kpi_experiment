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
