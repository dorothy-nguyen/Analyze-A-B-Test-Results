# Analyze-A-B-Test-Results
## Analyzing to understand the results of an A/B test run by an e-commerce website _ a project corresponds to Udacity - Data Analyst Nanodegree 
### 1. Introduction
A/B tests are performed prominently by data analysts and data scientists. For this project, I practice by inspecting the results of an A/B test run by an e-commerce website which has developed a new web page in order to convert users.  A/B test results are supposed to help the company understand if they should: (1) Implement the new webpage, OR (2) Keep the old webpage, OR (3) Perhaps run the experiment longer to make their decision. 

### 2. Software properties
The following versions of libraries were implemented to conduct the project:
- pandas==1.4.0
- numpy==1.22
- statsmodels==0.13
- matplotlib==3.5

### 3. Overview of project
This project includes three parts:

Part I: Probability
In this part, I started with the preliminary exploration of the data set, drops some incorrect observations, then I applied the probability to determine whether the new treatment group users lead to more conversions. The finding here stated that the new treatment page did not lead to more conversions.

Part II: A/B Test
To continue, I conducted a hypothesis test using bootstrapped samples based on the assumption that convertion rates of two pages are equal. Four steps of this A/B test are as follows: 
- Simulated (bootstrap) sample data set for both groups, and compute the conversion rate for those samples. 
- Used a sample size for each group equal to the ones in the cleaned data.
- Computed the difference in the conversion rate for the two samples above. 
- Performed the sampling distribution for the "difference in the conversion rate" between the two simulated-samples over 10,000 iterations; and calculated an estimate.
P-value suggests that there is no difference between the new and old pages since we can not reject null hypothesis at Type I error rate (0.05).

Part III: Regression
Lastly, I run a regression model to see if the results achieved in part II above can also be achieved by performing regression. Null and alternative hypotheses associated with this regression model were stated and verified using statsmodel. The result of regression model indicates that changing to the new page has zero effect on conversion.

### 4. Summary of main Findings
- The new treatment page was not better than the old control page in term of conversion rate.
- The country of the user did not seem to influence conversion rates between the treatment and control page.
- The company should keep the old page since it should be good for now. In addition, the company can always make another experiment in the future if the circumstances change.
