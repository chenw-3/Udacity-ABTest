# Udacity-ABTest
### A project on A/B testing I completed during my Udacity Nanodegree program 
#### Skills required: A/B Testing, Logistic Regression, Z-test
An online learning platform wants to test out a new program page layout to see if the new page converts more users to subscribers. An A/B test would be perfect for this analysis because it will provide the insight necessary to jugde whther the new page or the old page creates more subscribers by looking at the conversion rates of both pages and simulating the probabilty of a user converting or not. The experiment included separating users into two groups; the control and treatment goups. The control group received the old program page and the treatment group received the new program page. The error rate chosen was Type 1; the new page assumed to have a higher conversion rate even though the old page actually has a higher conversion rate.

### My null hypothesis is the old page converts more or about the same amount of users
#### -Null: P𝑜𝑙𝑑 >= P𝑛𝑒𝑤
#### -Alternative: P𝑜𝑙𝑑 < P𝑛𝑒𝑤
Here is what I did in my analysis:

* Cleaned the data by removing the instances where the control group received the new page and vice versa to ensure the data accurately represented the groups.
* Ensured that each User ID only occured once to prevent bias.
* The conversion rates for both groups were calculated based on the data:


Group  | # of participants  | Conversion Rates
------------- | ------------- | -------------
Control | 145274  | 0.120386
Treatment  |  145310 | 0.118808

* Ran a simulation to calculate the difference in conversion rates assuming the null is true. The p-value calculated from this simulation was 0.5039 which is greater than the 0.05 (Type 1 error rate) therefore we failed to reject the null hypothesis. 
* A logistic regression was done to test if the conversion rates were equal and based on the p-value of 0.19, it was was assumed to be true. 
* Other factors were then taken into consideration, i.e the country the user was in (Canada, the United Kingdom and the United States) but this turned out to not be an influential factor since the p-values were also higher than 0.05. 

### Summary:
The company should keep their old page until they can create a newer one that encourages users more to sign up for their learning programs.
