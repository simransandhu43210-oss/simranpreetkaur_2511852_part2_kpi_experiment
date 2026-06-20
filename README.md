# simranpreetkaur_2511852_part2_kpi_experiment
# Part 2: KPI Framework, Business Experiment Analysis & Decision Recommendation

## Business Problem Statement

### 1. What Decision Needs to Be Made
Should the new onboarding and activation campaign (Treatment) be launched 
to all users, replacing the existing onboarding experience (Control)?

### 2. Who the Decision Impacts
- New users signing up to the subscription-based digital product
- The product and growth teams responsible for user activation
- The business, which depends on paid conversions for revenue

### 3. What Metric Should Improve
The primary metric that must improve is the **Paid Conversion Rate** — 
the percentage of users who convert from free/trial to a paid subscription 
within 30 days. Supporting metrics include trial start rate and 
onboarding completion rate.

### 4. What Risks Must Be Monitored
- Refund rate (are converted users unhappy and requesting refunds?)
- Support ticket rate (is the new campaign causing user confusion?)
- Revenue per converted user (are we converting lower-quality users?)
- Engagement score drop (are users less engaged under the new campaign?)

### 5. What Evidence Is Required Before Making a Recommendation
- A statistically significant improvement in paid conversion rate 
  (p-value < 0.05) in the Treatment group compared to Control
- No significant increase in refund rate or support ticket rate
- Segment-level analysis to confirm improvement is consistent 
  across regions, device types, and plan types


  ## North Star Metric

### Selected North Star: Paid Conversion Rate
**Formula:** Users who converted to paid ÷ Total users in group

### 1. Why This Is the Main Success Metric
Paid Conversion Rate directly measures whether the campaign achieves 
its core business objective — turning free/trial users into paying 
customers. For a subscription-based company, every converted user 
generates recurring revenue. No other metric matters if users aren't 
converting to paid.

### 2. Why Other Metrics Are Supporting Metrics (Not North Star)

| Metric | Why It's Supporting, Not North Star |
|---|---|
| Landing Page Visit Rate | Users can visit but never convert — visiting alone generates no revenue |
| Trial Start Rate | Starting a trial doesn't guarantee payment |
| Onboarding Completion Rate | Completing onboarding is a step toward conversion, not conversion itself |
| Engagement Score | High engagement is good but doesn't directly = revenue |
| Average Revenue Per User | Depends on conversion happening first |

### 3. How This Metric Connects to Business Growth
More paid conversions = more recurring subscription revenue = 
company growth. If paid conversion rate improves by even 1%, 
across thousands of new users monthly, it compounds into 
significant revenue. This is the metric the CEO and investors 
care about most.

### 4. What Could Go Wrong If Optimized Blindly
- The campaign could pressure or trick users into converting, 
  leading to high refund rates immediately after payment
- We might convert a large number of low-value users who cancel 
  quickly, reducing average revenue per converted user
- Support tickets could spike if the campaign creates confusion, 
  increasing operational costs
- This is why guardrail metrics (refund rate, support ticket rate, 
  revenue per converted user) must be checked alongside conversion rate
