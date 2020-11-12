# YELP_UserCredibility

## Problem Statement and Hypothesis
This Project tries to develop a probability score for every user that determines up-to what extent can the user
be trusted. For achieving this score we will use the yelp elite users as the target variable to develop the models and use
their features ranked in the order of their importance to generate the score for each user.
Solving this problem is interesting because our score will be different and useful even when yelp already classifies
it’s users as Elite and Non Elite. YELP Elite status is something that can be obtained only if the user applies for it,
moreover , the elite users are very small in comparison (less than 5 percent). They are a many users who might not be
interested to apply for Elite status but still have a good profile and authentic reviews. Also, elite users might do a good
job but there is a high chances that they might not cover all details and explore every business in multiple locations.

## Approach
After performing classification, we use the feature importance from our classification to develop a score for every user,
this can be done by dot product of feature imp and respective variables. The scores of elite customers are separated
and log-graph of their scores is generated to fit a normal distribution and this can be used to calculate probability(our
measure of user credibility) by using mean and standard deviation from above elite user’s graph as input.

### Feature Importance after using LIGHTGBM classifier
<img src = "images/Image1.png">

### SHAP Plot
![](Image4.png)

### Elite User Log Score
![](/images/Image5.png)


### TNSE and Co-relation plots
![](/images/Image2.png)
![](/images/Image1.png)
