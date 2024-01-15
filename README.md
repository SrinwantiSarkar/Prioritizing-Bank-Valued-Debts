# Prioritizing-Bank-Valued-Debts

Prioritizing-Bank-Valued-Debts
This analysis delves into the handling of debts declared "uncollectable" by banks through a charge-off process. Despite this designation, my goal is to recover some owed money. To evaluate potential recovery, accounts are scored based on factors like the likelihood of payment and total debt. The bank implements various recovery strategies at different thresholds ($1000, $2000, etc.), intensifying efforts with higher expected recovery amounts. At the lowest level, automated systems are used, while higher levels involve human resources, incurring an additional $50 cost per level.

The critical question is whether the extra amount recovered at higher strategy levels surpasses the $50 additional cost, examining if there's a jump (discontinuity) of more than $50 in the recovered amount at higher strategy levels. The analysis utilizes a dataset, aiming to uncover patterns.

I focus on the transition between Level 0 and Level 1, occurring between Expected Recovery Amounts of $0 and $2000, with the transition threshold set at $1000. Level 1 customers (Expected Recovery Amounts between $1001 and $2000) receive more attention than Level 0 customers ($1 to $1000). To understand factors beyond Expected Recovery Amount across the $1000 threshold, I explore if customer age exhibits a jump at this point. Creating a scatter plot of age against Expected Recovery Amount in the range of $0 to $2000 covers Levels 0 and 1.

To ensure comparability of variables like age and sex above and below the $1000 Expected Recovery Amount threshold, I aim to rule out differences in these variables as the cause for variations in the actual recovery amount. The Kruskal-Wallis test is employed to assess significant differences in ages above and below the threshold, focusing on the range from $900 to $1100.

With no significant jump in average customer age around the $1000 threshold, attention shifts to the percentage of male customers. Statistical analysis, including cross-tabs and chi-square tests, is conducted for the percentage of male versus female customers in the range of $900 to $1100.

Having established similarity between customers above and below the $1000 threshold, I shift focus to the key outcome: the actual recovery amount. A scatter plot explores the relationship between expected and actual recovery amounts, emphasizing the range just below and just above the $1000 threshold.

Statistical tests are employed to assess if there's a discontinuity in the actual recovery amount above the $1000 threshold, using different windows of expected recovery amounts: $900 to $1100 and a narrower range of $950 to $1050. The Kruskal-Wallis test is applied to determine significant differences in actual recovery amounts above and below the threshold.

In regression modeling, two models are built. The first predicts the actual recovery amount as a function of the expected recovery amount, examining the adjusted R-squared to gauge the percentage of variance explained. The second model adds an indicator of the true threshold at $1000, assessing the additional amount recovered due to the higher recovery strategy.

Adjusting the expected recovery amount window, the regression coefficient for the true threshold remains statistically significant with an estimated impact much larger than the $50 per customer cost for the higher recovery strategy. Consistency across wide ($900 to $1100) and narrower windows ($950 to $1050) reinforces the conclusion that the higher recovery strategy is worth the extra $50 cost per customer.
