# Topic

Hypothesis Testing Assignment - Ordered choice model.

**Data from 2 sources, go to 'How to access the data' for instructions.** 

I perform hypothesis testing, using the probit and logit models to find out why some of our subjects (6,366 married women) cheated during their marriage and why some do not **(Q1)**. 

I will also use the Poisson model for count data to estimate the number of hospital visits based on the household’s income, including household monthly net income, marriage, and employment **(Q2)**.


## Main learning components

* Ordered choice models: probit and logit. 
* Poisson model for count data.
* Report the regression results and the marginal effects.
* Estimate the model using ordinary least squares.
* Test for overdispersion.

# How to access the data - Q1

Table F17.2 ([http://pages.stern.nyu.edu/~wgreene/Text/Edition7/tablelist8new.htm](http://pages.stern.nyu.edu/~wgreene/Text/Edition7/tablelist8new.htm)) provides Fair’s (1978)  _Redbook_  survey on extramarital affairs. The variables in the data set are as follows:

**_id_  = Identification number,**

**_C_  = Constant, value = 1,**

**_yrb_= Constructed measure of time spent in extramarital affairs,**

**v_1_ = Rating of the marriage, coded 1 to 4,**

**_v2_  = Age, in years, aggregated,**

**_v3_  = Number of years married,**

**_v4_  = Number of children, top coded at 5,**

**_v5_  = Religiosity, 1 to 4, 1 = not, 4 = very,**

**_v6_  = Education, coded 9, 12, 14, 16, 17, 20,**

**_v7_  = Occupation,**

**_v8_  = Husband's occupation.**
​
And three other variables that are not used. The sample contains a survey of 6,366 married women, conducted by  _Redbook_  magazine. For this exercise, we will analyze, first, the binary variable

**_A_  = 1 if  _yrb_  > 0, 0 otherwise.**
## Q1 - Questions
a) The regressors of interest are  _v1_  to  _v8_; however, not necessarily all of them belong in your model. Use these data to build a binary choice model for  _A_. Report all computed results for the model. Compute the marginal effects for the variables you choose. Compare the results you obtain for a probit model to those for a logit model. Are there any substantial differences in the results for the two models?

b) Continuing the analysis from part a), we now consider the self-reported rating,  _v1_. This is a natural candidate for an ordered choice model, because the simple five-item coding is a censored version of what would be a continuous scale on some subjective satisfaction variable. Analyze this variable using an ordered probit model. What variables appear to explain the response to this survey question? Can you obtain the marginal effects for your model? Report them as well. What do they suggest about the impact of the different independent variables on the reported ratings?

# How to access the data - Q2
The German health care data include a count variable, DocVis, which is the reported number of visits to the doctor. The data are described in Table F7.1
([http://pages.stern.nyu.edu/~wgreene/Text/Edition7/tablelist8new.htm](http://pages.stern.nyu.edu/~wgreene/Text/Edition7/tablelist8new.htm)). A second count variable in that data set is  _HospVis_, the number of visits to hospital. For this application, we will examine this variable. To begin, we treat the full sample (27,326) observations as a cross section.
What you need to do is click on the link (Table F7.1) that takes you to the JAE Archive. The data is in the folder named "rwm-data.zip." Note that it’s in  **.data**  format and you can open that in Excel. Here are the steps for opening the  **.data**  file in Excel:

**i. File Open**

**ii. Select “All Files”**

**iii. Select your .data file**

**iv. Select “fixed width”**

**v. Finish**

Now you can label the columns/variable names using the "readme file" in the JAE Archive. Please follow the variable order in the "readme file."

## Q2 - Questions
a) Begin by fitting a Poisson model to this variable. The exogenous variables are listed in Table F7.1. Determine an appropriate specification for the right-hand side of your model. Report the regression results and the marginal effects.

b) Estimate the model using ordinary least squares and compare your least squares results to the marginal effects computed in part a). What do you find?

c) Is there evidence of overdispersion in the data? Test for overdispersion.
# Visualizations
**![](https://lh4.googleusercontent.com/5oZ1wdH3ZuIZ1u1rrXVkeDUFlcdM7PIiWeML2sajQ0oio9Hn6FHII957en6Lcxrl9UG4_x4ScjSvI9EOHP_kYP5EhQ0j5hxbN3NGG_YsTDg-z0NcmPbLBUpS5Q02v2eKMGjKQKOKQf8)**
**![](https://lh3.googleusercontent.com/9w8Zi647DCF67-qWG6xzmBS0DksQmch8IO8n1jHirXdMFxV4btCvPx22L3t0eWeDgkq5OUHwvY1H7WIxYQxEOZ4o_MvKKX6IolgRfTkWU6CUHFT24Kd8kawRQTwzuH9obcuStmOSgHE)**
**![](https://lh6.googleusercontent.com/CWnhgMAwLhJfcJ4ty04YBANVh8svGtJCwjpOVM2CUCsUXUyP5Sypf7LluNdXbAOTrFCVi4XQa-a1yfZfA0kgz_b5QxNgz_-pDI2xu7owj_ar3QpyTVK6B3xi15RQKBPehCcUn9IrQlU)**
**![](https://lh4.googleusercontent.com/FhMYNgyo1QbGDglanEjtZAQJxvgXfeZXoxtmxePE33OTB8cWs-4l6BwRz9WeGaPYskDD3yTqpusvkceym4ISO7cRme6vlsnKr9Q6HMW-ysGeDaMGuJFlLJcNY0uhu41C0kXMcyJXZ5k)**

# Conclusion
## Q1
From the table of the probit model, we can see that variables v3 and v7 are statistically significant while v4 and v8 are not. There is a 0.3 point increase in the likelihood of cheating with each additional year in marriage (v3). 
Similarly, there is a 3% increase correlated with the women’s occupation. ​The marginal effects​ of the probit model tells us the ​ceteris paribus effects of changes in the variables chosen for the regression. Again, we see that variable v4, indicating the number of children is not statistically significant, implying that the number of children will not explain the cheating pattern among married women. 
**We can see from the table that a one unit increase in variables v3 (year in marriage) and v7 (wife occupation) both correlates with a 0.1 point increase in likelihood of cheating. As such an increase in real terms is not a huge number, variables ​v3​ and v7 cannot act as standalone explanatory variables for the cheating pattern among married women. Although these two variables are statistically significant, they do not have a strong causation relationship with our dependent variable.**

Variable ​v1​ is a self-reported rating of married women on their marriage, which can be a proxy for their level of satisfaction of the marriage. I will treat variables ​v2 t​ o ​v8​ as independent variables that influence the ratings each woman gives to their marriage. ​We can see from the p-values that variables ​v4,​ ​v5​, ​v6​, and ​v8​ are statistically significant while variables ​v2,​ ​v3​, ​v7​ are not. Generally, for a unit increase in marriage rating there is an unit increase in the percentage of education (v5), religiosity (v6), and husband occupation (v8). There is a unit decrease in marriage rating with every increase in the number of children (v4).
The marginal effects for this model tells us which rating score women will likely give under each condition, and we may be able to observe a trend. **The same pattern for education is reflected for variable ​v8,​ which is a proxy for husband’s occupation. In short, marginal effects on the ordered probit model is useful for variables that contain rates or ordered choices like ​v1​ as it shows the likelihood for each score under each independent factor, as opposed to all factors together.**


## Q2

The Poisson model is used for count data like the German health care data, which counts the number of occurrences of an event (visits to the hospital). This model differs from other probability models because the data is discrete, not continuous, and has no negative data points.

The results show that the education (​educ​) and employment (​working​) variables are statistically significant, while the marriage variable is not. With each increase in the years of schooling, an individual has 7% fewer hospital visits and employment means that an individual has 26% fewer hospital visits. The marginal effects tell us that with a unit increase in years of schooling and an increase in chance of employment, an individual will have 0.01 and 0.03 fewer hospital visits, respectively.

Using an ordinary least squares model, the results for hospital visits based on years of schooling and employment are similar to that obtained with the marginal effects of the Poisson model. The coefficients for ​educ​ and ​working​ are 0.087 and 0.04 which is quite close to the respective 0.01 and 0.03 results presented above.


## Test for overdispersion
When testing for overdispersion, we are looking out for a large standard deviation, which can indicate that the data is not a good fit. The results for the goodness-of-fit test are extreme values, which indicates that the test is not appropriate for our case. Thus, we move on to check for overdispersion using the negative binomial regression. The p-value shows us that this model is statistically significant. However, the alpha value at the bottom of the table is 8.6 which is statistically different from zero, and thus, proves that the negative binomial model is different from the Poisson model, or would not yield similar results to the Poisson model. Therefore, we conclude again that there is overdispersion in the Poisson model.
