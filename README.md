# Responsible Machine Learning - Bias Testing & Remediation
# (Assignment 3)

## Q1) Test model for Bias using AIR
### Bias in Machine learning
* **Machine learning bias generally stems from problems introduced by the individuals who design and train the machine learning systems. They could either create algorithms that reflect unintended cognitive biases or real-life prejudices. Or they could introduce biases because they use incomplete, faulty or prejudicial data sets to train and validate the machine learning systems.**
* The following definitions are taken from PiML website.
* **In PiML we use 'Model fairness'to evaluate 'Metrics','Segmentation','Binning','Thresholding'.**
* **"Metrics measure the Adverse Impact Ratio (AIR),Precision,Recall,Standarized Mean Difference(for regression task)".**
* **Segmentation:"It is used to display fairness results conditioning on a feature of interest.So we may effectively analyze and evaluate fairness at a granular level, allowing for a more comprehensive understanding of the model’s fairness performance across various segments of the data."**
* **Feature Binning:"It is  used to  discretize / bin feature values that may lead to unfair results. There are three binning methods, quantile, uniform, and customize.It is one of the unfairness mitigation method"**
* **Thresholding:"It is another unfairness mitigation method wherein we enumerate the classification threshold to get a better trade-off between fairness and performance. The keyword for this strategy is “thresholding” for the show parameter."** 

### Categorizing Race & Gender

<br>
<br>

<br>

<div align="center">
 
![pfi  x](https://github.com/thebader9/RMLGROUP2/assets/111473895/97224b8e-0c13-492e-9a2c-e7e6f6da35ed)
 
 
 <div align="center">
 <img src="https://github.com/thebader9/RMLGROUP2/assets/111473895/8ad88091-6b8a-4475-a334-a1bcfbee5c0f" alt="Image" width="530" height="120">
  
  
 <!-- Add some vertical space -->
<br>
<br>

<br>
<br>
<br>

![pfi  x](https://github.com/thebader9/RMLGROUP2/assets/111473895/c180e50c-6eee-42e7-a982-82207e78f063)



![pfi  x](https://github.com/thebader9/RMLGROUP2/assets/111473895/e6807a80-7333-4e85-b9ee-39e9f4c37ec6)
* ** **


![pfi  x](https://github.com/thebader9/RMLGROUP2/assets/111473895/32f8e638-7d73-4628-8801-1d10fad17287)
* ** **


![pfi  x](https://github.com/thebader9/RMLGROUP2/assets/111473895/c310d639-ed89-427d-8019-7528abd04666)
* ** **



#####
![pfi  x](https://github.com/thebader9/RMLGROUP2/assets/111473895/14619585-f763-4a27-aa36-b442d2c51b0c)
* ** **

### Segmentation

##### Intro_rate_period_std

![pfi  x](https://github.com/thebader9/RMLGROUP2/assets/111473895/b8344d0a-dea5-4df0-ba61-5bd8bb4fa195)

![pfi  x](https://github.com/thebader9/RMLGROUP2/assets/111473895/113fd6f9-beef-4889-82ff-fd2439f89035)


##### Property_value_std

![pfi  x](https://github.com/thebader9/RMLGROUP2/assets/111473895/a9213192-08d9-44ba-ae52-e5838cccf68c)
![pfi  x](https://github.com/thebader9/RMLGROUP2/assets/111473895/20e93dfd-3a43-4568-89ca-ad6fb64755c7)



##### Loan_amount_std

![pfi  x](https://github.com/thebader9/RMLGROUP2/assets/111473895/a09c9161-6595-4aca-bc60-659e90973665)

![pfi  x](https://github.com/thebader9/RMLGROUP2/assets/111473895/71b545bd-3336-460c-89d3-b6cb8f20d48c)

##### Income_std
![pfi  x](https://github.com/thebader9/RMLGROUP2/assets/111473895/d637c02f-0ddf-4879-bc1b-05b0fe3d7e87)
![pfi  x](https://github.com/thebader9/RMLGROUP2/assets/111473895/6a48fe6e-bb01-491b-9db3-b7f1c816ba93)

#### Conforming
![pfi  x](https://github.com/thebader9/RMLGROUP2/assets/111473895/7eef28c6-180c-4f59-af1a-008f945da5a0)
![pfi  x](https://github.com/thebader9/RMLGROUP2/assets/111473895/29df5850-78ae-4d73-b6d1-53bb9c1894f1)




## Q2)Remediate discovered Discrimination













# Responsible Machine Learning - Post hoc explainability 
# (Assignment 2)

## Q1) Global Explainability and Interpretability

### Global Explainability im PiML

#### Permutation Feature Importance (PFI)
* **Permutation Feature Importance (PFI): Computes the change in prediction performance as the measure of feature importance. Breaks the relationship between the feature and the target, thus the drop in the model score is indicative of how much the model depends on the feature**

##### EBM
![pfi ebm](https://github.com/thebader9/RMLGROUP2/assets/111529115/7e4800b4-5e00-40ad-a8d7-6faf8c19da59)
* **‘loan_to_value_ratio_std’ is the most influential feature in this model**
* **‘Property_value_std’, ‘Debt_to_income_ratio_std’, ‘loan_amount _std’ have a significant impact on the target variable (high priced)**

##### ReLU-DNN

![PFI Relu](https://github.com/thebader9/RMLGROUP2/assets/111529115/bad62191-d066-40ae-b379-74cbc54ba736)
* **‘Property Value’ is the most influential feature in this model**
* **‘Loan to value ratio’, ‘loan amount’, ‘debt to income ratio’ have a significant impact on the target variable (high priced)**

##### XGB2
![pfi  x](https://github.com/thebader9/RMLGROUP2/assets/111529115/e1716e36-8480-4ec8-9552-6385cfbd65be)
* **Loan_to _value _ratio_ std, Property value std and debt to income ratio std are the top three features that play pivotal role in deciding high_priced_mortagage among other features.**


### Global Interpretability im PiML

#### Feature Importance (FI)

##### EBM
![global ebm](https://github.com/thebader9/RMLGROUP2/assets/111529115/37b2929f-e304-43af-a287-6833c502110a)
* **The most influential features when predicting High Priced are loan_to_value_ratio_std, Property_value_std, Debt_to_income_ratio_std.**

##### ReLU-DNN
![global relu](https://github.com/thebader9/RMLGROUP2/assets/111529115/edc766d2-8c88-4994-96a1-d7cfd1acf93f)
* **The most influential features when predicting High Priced are Loan to value, Property Value, loan amount, and Intro Rate period.**

##### XGB2

![global x](https://github.com/thebader9/RMLGROUP2/assets/111529115/70eb03d3-2093-4bc2-87c3-57d175659e9f)
* **Loan_to _value _ratio_ std, Property value std and debt to income ratio std are the top three features that play pivotal role in deciding high_priced_mortagage among other features.**


## Q2) Local Explainability and Interpretability

#### Local Explainability/Interpretability

* **LIME: Explains creating a surrogate (smaller, simpler) model. Then approximates predictions
The "effect" in LIME refers to the impact of each feature on the predicted outcome for the selected instance. Positive coefficients indicate that the feature has a positive effect on the prediction, while negative coefficients indicate a negative effect.**

* **SHAP:F(x) refers to the prediction of the machine learning model for a given data point x, while E[F(x)] refers to the expected prediction of the model over a background dataset.
If F(x) and E[F(x)] are close to each other, it suggests that the model is making predictions that are consistent with the overall behavior of the dataset.If there is a large difference between F(x) and E[F(x)], it suggests that the model makes predictions that are significantly different from the overall behavior of the dataset, which may indicate bias or overfitting.Positive values indicate that the feature contributes positively to the prediction, while negative values indicate that the feature contributes negatively. The size of the SHAP value indicates the magnitude of the feature's influence.**

#### EBM

##### Sample 30
![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/32ba615f-02ea-48d9-89d1-e4793f6e32a2)
* E[f(X)]= 0.082 represents the average predicted output over the background data .
* F(X) = 0.125 that predicts sample index for 30 .

* Shap: lone _to _value _ratio_std  has a SHAP value of 0.05 and contributes the most positive affect , followed by income std , which has a SHAP value of   -0.01 its means negative affect on mortgage high price .
* lime: lone _to _value _ratio_std  has a SHAP value of contributes the most positive affect , followed by property_value_std  negative affect on mortgage high price .

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/cd91b7e3-fe9e-4824-9659-b89c6f636670)
* Local Interpretability:  The title indicates that the predicted value for this sample is 0.1268, which differs slightly from the actual response of 1.0000.The     main effect of lone _to _value _ratio_std makes the largest contribution to the final prediction, with a positive effect (approximately0.95). Second number       property_value contribution  to the final prediction, with a positive effect (approximately0.20) on mortgage high price.


##### Sample 8000
![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/a0bafc1b-eea9-4071-83ff-8f07ae08f879)
* E[f(X)]= 0.082 represents the average predicted output over the background data .
* F(X) = 0.005  that predicts sample index for 8000.

* shap:  loan _to _value _ratio_std  has a SHAP value of - 0.04 and contributes the most negative effect , followed by term 360   ,which has a SHAP value of -0.02 this  effect also negative  effect high-priced mortgage.
* lime: loan _to _value _ratio_std  contributes the most postive effect high-priced mortgage.

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/86b19a24-13c5-4303-a1b9-6ad69a22f08b)
 * Local Interpretability: The title indicates that the predicted value for this sample is 0.0052, which differs slightly from the actual response of 0.0000.The     main effect of loan _to _value _ratio_std makes the largest contribution to the final prediction, with a Negative effect (approximately – 0.05).  Second           numberterm_360 contribution to the final prediction, with a negative  effect (approximately- 1.2) on mortgage high price.
 


##### Sample 16000

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/2f38089a-8496-49fa-a2d2-c91b8d9188c6)
* shap: loan _to _value _ratio_std  has a SHAP value of - 0.04 and contributes the most negative effect , followed by Property_value_std ,which has a SHAP value     of -0.02 this  effect also negative  effect on high-priced mortgage.
* lime : debt_to_income_ratio_std contributes the most postive effect high-priced mortgage.

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/66a2c226-05ba-41c1-86a7-37ebb38f12f3)
* Local Interpretability: The title indicates that the predicted value for this sample is 0.0073, which differs slightly from the actual response of 0.0000.The main effect of loan   _to   _value _ratio_std makes the largest contribution to the final prediction, with a Negative effect (approximately – 0.05). Second number property_ value contribution to the final prediction, with a negative  effect (approximately-0.5) high-priced mortgage.

#### Reul-DNN

##### Sample 30
![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/2644632f-d02c-47dc-9a61-7d708863155f)
* SHAP: Loan to value ratio, property value, and loan amount are the most important features in predicting High Priced. They all have a positive relationship with the target variable.
* LIME: Agrees with SHAP for Loan to value ratio, property value, and loan amount to be the most important features in predicting High Priced.

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/180ed519-7799-4276-936d-14f4a7109237)
* Local Interpretability: Agrees with LIME that property value is the most important feature in predicting the target variable.



##### Sample 8000
![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/593caa41-8a1f-44a4-9ae1-580f5071ca8f)
* SHAP: Loan to value ratio, property value, and term 360 are the most important features in predicting High Priced. They all  have a negative relationship with the target variable.
* LIME: Agrees with SHAP for Loan to value ratio, property value, and term360 to be the most important features in predicting High Priced. But has term360 as the   most important.

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/a60bbecb-1b2a-44c5-bd59-b0b8700eef29)
* Local Interpretability: Agrees with LIME that term360 is the most important feature in predicting the target variable.



##### Sample 16000

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/ce332882-692b-44e2-8de1-addf1980c104)
* SHAP: Loan to value ratio, property value, and loan amount are the most important features in predicting High Priced. Loan to   value ratio and property value have a positive relationship with the target variable. While loan amount has a negative relationship with the High Priced.
* LIME: Agrees with SHAP for property value to be the most important feature in predicting High Priced, but followed by debt to income ratio


![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/d1bcad6f-46d8-4976-9dc4-e76cafba33d5)
* Local Interpretability: ‘no intro rate period’ feature is the most important feature, followed by debt to income ratio.

#### XGB2

##### Sample 30

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/bac54f76-c238-43cc-a287-486ea770794b)


* **LIME and SHAP agrees on the most influential feature to be  loan_to_value_ratio_std with a positive effect on high_priced_mortgage for sample point 30.**

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/549846bc-1595-49c9-a96d-823be477ca16)

* Local Interpretability:As shown in the model above ‘loan_to_value_ratio_std’ feature represent the standardized ‘loan-to value-ratio’, which is a measure of the loan amount relative to the appraised value of the property.A higher loan-to-value ratio indicates a higher risk for lenders,potentially leading to higher interest rates and hence the value of 0.5525 suggest that the loan to value ratio for this particular application is relatively high.**


##### Sample 8000

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/13d07c5a-3422-4ad5-96b1-f29d1cda1bea)

* **LIME and SHAP disagree on the most influential feature on ‘high_priced_mortgage’ for Sample point 8000. LIME suggests that ‘loan_to_value_ratio_std’ is the most influential feature with a positive  effect on ‘high_priced_mortgage’, while SHAP suggests that ‘property_value_std’ is the most influential with a negative effect on ‘high_priced_mortgage’.**


![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/612cb739-42d3-4802-9b3a-0ef42c5acfc1)

* Local Interpretability:Property value, loan-to-value ratio, and term_360, are directed towards the left side, indicating that decreasing or lower values of these features for a specific instance have a relatively stronger influence on the prediction of a high-priced mortgage.**


##### Sample 16000

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/0da78f03-3be8-4148-a087-00846158d418)

* **LIME and SHAP agree that ‘loan_to_value_ratio_std’  has the strongest influence on ‘high_priced_mortgage’ for sample point 16000. ‘Loan_to_value_ratio_std’has a negative effect on‘high_priced_mortgage’ as the value is -0.04 . LIME and SHAP disagree on the rankings and effects of the other features on Status.**

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/70131d55-378a-46a9-90a1-655df4f18057)

* Local Interpretability:Property value, loan-to-value ratio, play pivotal role in predicting ‘high_priced_mortgage’ and are directed towards the left side, indicating that decreasing or lower values of these features for a specific instance have a relatively stronger influence on the prediction of a high-priced mortgage.**






## Q3) Feature Behavior
### Partial Dependency Plot (PDP) and Accumulated Local Effects (ALE)
* **Partial Dependence Plot (PDP): used to understand how the prediction varies as a function of variables of interest, by averaging over other variables.Not recommended if the features are correlated**

* **Accumulated Local Effects (ALE): describes how features affect a model prediction.It shares the same goal as PDP (Partial Dependence Plot).Overcomes the features correlation problem by averaging and accumulating the difference in predictions across the conditional distribution, limiting the effects of specific features.**

##### EBM

##### loan_to_value_ratio_std

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/fa1f0b57-df28-4559-b79e-624135122bd9)

* **There is a negative relationship between ‘mortgage is high priced’ and ‘loan_to_value_ratio_std’. As ‘loan_to_value_ratio_std’ increases, the probability of that individual’s mortgage to be ‘high priced’ decreases. There is a hike at first because the relationship is positive if the value of ‘loan_to_value_ratio_std’  is less than 0.**

##### Debt_to_income_ratio_std

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/ec8fa39d-005c-4904-9ae7-769e95e6be39)

* **There is a negative. relationship between ‘mortgage is high priced’ and ‘Debt_to_income_ratio_std’ when the value is less than 1. As ‘Debt_to_income_ratio_std’  increases, the probability of that individual’s mortgage to be ‘high priced’ increases, up until the ratio is at around 1, then the relationship is positive .**

##### Property_value_std

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/e46f176f-e46d-4cf2-bbdb-1b4781489d51)

* **There is a negative relationship between ‘mortgage is high priced’ and ‘Property_value_std’. As Property_value_std’ increases, the probability of that individual’s mortgage to be ‘high priced’ decreases.**                       


##### Loan_amount_std

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/d34126b6-1cdc-419d-b514-648e27870d7c)

* **There is a negative relationship between ‘mortgage is high priced’ and loan_amount_std. As ‘loan_amount_std’ increases, the probability of that individual’s mortgage to be ‘high priced’ decreases.**



##### Intro_rate_period_std

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/4596282f-2cf8-4312-a555-ec3b21d6cd04)

* **Both PDP and ALE agree that there’s a positive relationship until the value of ‘Intro_rate_period_std’ is at around 6.6 and ALE 3.3 then there’s positive relationship at both PDP and ALE.**


##### Income_std

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/e08d3c59-c99c-40ce-b03e-b2a5d5f60277)


* **There is a Positive relationship between ‘mortgage is high priced’ and ‘Income_st:’. As ‘Income_std’ increases, the probability of that individual’s mortgage to be ‘high priced’  increases. In both PDP and ALE.**
 
                      
##### No_intro_rate_period_std

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/1d90816e-b909-4a18-b962-3568d2697708)

* **This suggests that the variable does not have a significant impact on the outcome being measured when it is at extremely low values,negative effect on the accumulated local effect.From the ALE plot for the categorical feature No_intro_rate_period_std . From this plot, we can see that No_intro_rate_period_std  with values 0.2444 have a significantly negative effect on the final prediction, as compared to -4.091.**
      
                        
##### Term_360

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/9914f195-98cd-468f-ab8f-6c6261524f4e)

* **From ALE plot for the categorical featureTerm_360  . From this   plot, we can see that Term_360 with values 1 have a significantly negative effect on the final prediction, as compared to 0.**
 
                     
##### Conforming

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/6d8b3789-a6d3-460e-918c-d64a07d84f38)

* **This is the ALE plot for the categorical feature conforming  . From this   plot, we can see that conforming   with values 1 have a significantly negative effect on the final prediction, as compared to 0.**
                       
##### debt_to_income_missing

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/6db7a035-017c-42fd-b127-a56662e8c48e)

* This is the ALE plot for the categorical feature debt_to_income_missing: . From this  plot, we can see that debt_to_income_missing: with values 1  have a significantly negative effect on the final prediction, as compared to 0. 



##### ReLU-DNN

##### loan_to_value_ratio_std
![PFIRELU](https://user-images.githubusercontent.com/111473895/244163945-c878131b-cd05-4288-960a-ce1e93a10cc0.png)
* **There is a negative relationship between ‘mortgage is high priced’ and ‘loan_to_value_ratio_std’ when the value is above 0. As ‘loan_to_value_ratio_std’ increases, the probability of that individual’s mortgage to be ‘high priced’ decreases. There is a hike at first because the relationship is positive if the value of ‘loan_to_value_ratio_std’ is less than 0.**

##### Debt_to_income_ratio_std
![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/46a63e44-91e8-4e89-a9ff-99991c2a16ff)
* **There is a positive relationship between ‘mortgage is high priced’ and ‘Debt_to_income_ratio_std’ when the value is less than 1. As ‘Debt_to_income_ratio_std’  increases, the probability of that individual’s mortgage to be ‘high priced’ increases, up until the ratio is at around 1, then the relationship is negative.**

##### Property_value_std

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/28b7a939-a871-46a7-8bc9-f804adccf652)
* **There is a negative relationship between ‘mortgage is high priced’ and ‘Property_value_std’. As Property_value_std’ increases, the probability of that individual’s mortgage to be ‘high priced’ decreases.**


##### Loan_amount_std

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/97b0f45e-0875-4309-978d-c9898a1f912d)
* **There is a negative relationship between ‘mortgage is high priced’ and loan_amount_std. As ‘loan_amount_std’ increases, the probability of that individual’s mortgage to be ‘high priced’ decreases.**


##### Intro_rate_period_std

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/37eec072-da24-4e93-9022-fad32e5753f7)
* **Both PDP and ALE agree that there’s a positive relationship until the value of ‘Intro_rate_period_std’ is at around 3.3 then there’s positive relationship at PDP while it’s negative at ALE.**

##### Income_std

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/7216d043-1fb6-4fb3-8ec9-c3f343c955ed)

* **There is a negative relationship between ‘mortgage is high priced’ and ‘Income_st:’. As ‘Income_std’ increases, the probability of that individual’s mortgage to be ‘high priced’ decreases.**

##### No_intro_rate_period_std

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/3534adf5-757a-48e3-9377-db4699f6f8c1)
* **The PDP graph suggest the ‘absence of an introductory rate period (1) ‘is associated with a slightly higher likelihood of a high-priced mortgage.However, in ALE the result are different where ‘ absence of introductory rate period (1)’ ) does not strongly influence the probability of a high-priced mortgage.**


##### Term_360

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/b7a1190a-05d3-4476-ade4-ea2dc40b0212)
* **The PDP graph indicates that having a standard 360 month mortgage (1) is associated with a slightly higher likelihood of a high-priced mortgage, while the ALE graph shows that having a standard 360 month mortgage (1) does not strongly influence the probability of a high-priced mortgage.**

##### Conforming

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/42474987-680f-49ee-8178-3fbdd251912f)
* **The PDP chart indicates that having a conforming mortgage (1) is associated with a higher likelihood of a high-priced mortgage, while in ALE it shows that having a conforming mortgage (1) is associated with least likelihood of getting a high priced mortgage as it is close to 0.**

##### Debt_to_income_ratio_missing

![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/6536c3a7-a8f4-4325-acd4-eecc833a8fec)
* **Both PDP and ALE represent that the presence of higher debt to income ratio(1) will lead to high priced mortgage.**




##### XGB2

##### Loan_to_value_ratio_std
![PFIXGB2](https://user-images.githubusercontent.com/111473895/244147475-4dbd54ca-7e0d-4e4f-8c8f-81323b6eed5c.png)

* **As seen in ALE there is a positive relationship between loan_to_value_ratio_std and high_priced_mortgage. As loan_to_value_ratio_std increases, the probability of that individual for getting high_priced_mortgage increases.However PDP is constant at certain points and this doesn’t have effect on behavior.**

##### Property_value_std
![PFIXGB2](https://user-images.githubusercontent.com/111473895/244149016-205f4396-cd74-4610-8afe-949ce00598e0.png)
* **There is a negative relationship between property_value_std and high_priced_mortgage as seen in ALE.As loan_to_value_ratio_std increases,the probability of getting high_priced_mortgage decreases.**

##### Debt_to_income_ratio_std
![PFIXGB2](https://user-images.githubusercontent.com/111473895/244149147-94a77ca7-352c-444e-86cb-8c6949a2cf3f.png)
* **As seen in ALE there is a positive relationship between debt_to_income_ratio_std and high_priced_mortgage. As loan_to_value_ratio_std increases, the probability of getting high_priced_mortgage increases.In PDP however the probability of that individual’s mortgage to be ‘high priced’ increases, up until the ratio is of around 0.7, then the relationship is negative.**


##### loan_amount_std

![PFIXGB2](https://user-images.githubusercontent.com/111473895/244149288-14e2825a-b9c4-487a-87cd-7c0d0b17ad5d.png)
* **As seen in PDP the likelihood of a high priced mortgage goes up with increase loan amount and has positive relationship with loan amount. The feature in global explain ability ranks low compared to other features so the importance of this prediction in overall model predictability is low.**

##### Income_std

![PFIXGB2](https://user-images.githubusercontent.com/111473895/244149480-80f6979c-c03a-4d2f-b57c-78bbb41596ca.png)
* **There is a negative relationship between ‘mortgage is high priced’ and income _std. As ‘income _std’ increases, the probability of that individual’s mortgage to be ‘high priced’ decreases.**

##### Intro_rate_ period 

![PFIXGB2](https://user-images.githubusercontent.com/111473895/244149555-99592278-78ad-4d85-9469-169db4a661c9.png)
* **As seen in ALE the maximum probability of high priced mortgage is at the value of 0.1 of intro_rate_ period and then there is negative relationship.The feature in global explainability ranks low compared to other features so the importance of this prediction in overall model predictability is low.**

##### No_intro_rate_period_std

![PFIXGB2](https://user-images.githubusercontent.com/111473895/244149598-24ad36bb-1d52-4893-9433-e3a0191b1631.png)
* **The PDP graph suggest the ‘absence of an introductory rate period (1) ‘is associated with a slightly higher likelihood of a high-priced mortgage.However, in ALE the result are different where ‘ absence of introductory rate period (1)’ ) does not strongly influence the probability of a high-priced mortgage.**

##### Term_360

![PFIXGB2](https://user-images.githubusercontent.com/111473895/244149643-f984ec2c-6ee9-4ba2-b391-67811c9d862c.png)
* **The PDP graph indicates that having a standard 360 month mortgage (1) is associated with a slightly higher likelihood of a high-priced mortgage, while the ALE graph shows that having a standard 360 month mortgage (1) does not strongly influence the probability of a high-priced mortgage.**


##### Conforming
![PFIXGB2](https://user-images.githubusercontent.com/111473895/244149687-2c42f0ff-e398-4e39-a74b-fba77398de9a.png)
* **The PDP chart indicates that having a conforming mortgage (1) is associated with a higher likelihood of a high-priced mortgage, while in ALE it shows that having a conforming mortgage (1) is associated with least likelihood of getting a high priced mortgage as it is close to 0.**

##### Debt to income ratio

![PFIXGB2](https://user-images.githubusercontent.com/111473895/244149714-d6efafe4-1786-48c8-bf29-d2b11659b720.png)
* **Both PDP and ALE represent that the presence of higher debt to income ratio(1) will lead to high priced mortgage.**
