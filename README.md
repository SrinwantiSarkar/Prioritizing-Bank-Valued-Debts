# Prioritizing-Bank-Valued-Debts  
**Background**:
Analysis of handling "uncollectable" debts by banks through charge-off.
Goal: Recover owed money by scoring accounts based on factors like payment likelihood and total debt.

**Recovery Strategies:**
Implemented at various thresholds ($1000, $2000, etc.).
Higher expected recovery amounts entail more effort.
Levels:
Level 0: Expected recovery amounts > $0 and <= $1000.
Level 1: Expected recovery amounts > $1000 and <= $2000.
Automated systems at Level 0, human resources at higher levels, incurring $50 additional cost per level.

**Transition Analysis**:
Focus on Level 0 to Level 1 transition.
Transition threshold at $1000.
Level 1 customers (Expected Recovery Amounts $1001-$2000) receive more attention.

**Exploratory Analysis**:
Examining factors beyond Expected Recovery Amount:
Age analysis: No significant jump around $1000.
Gender analysis: Ensuring comparability in the percentage of male customers.

**Scatter Plot Analysis**:
Relationship between expected and actual recovery amounts.
Emphasis on the range just below and above $1000 threshold.

**Statistical Tests**:
Kruskal-Wallis test to assess differences in ages above and below the threshold.
Cross-tabs and chi-square tests for the percentage of male versus female customers.

**Regression Modeling**:
Two models built:
Model 1: Predicts actual recovery amount as a function of expected recovery amount.
Model 2: Adds an indicator of the true threshold at $1000.

**Adjusting Windows**:
Regression coefficient for the true threshold remains statistically significant.
Estimated impact much larger than $50 per customer cost for the higher recovery strategy.
Consistency across wide ($900 to $1100) and narrower windows ($950 to $1050).

**Conclusion**:
Higher recovery strategy worth the extra $50 cost per customer.
