# Responsible Machine Learning - Post hoc explainability (Assignment 2)

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



## Q3) Feature Behavior
### Partial Dependency Plot (PDP) and Accumulated Local Effects (ALE)
* **Partial Dependence Plot (PDP): used to understand how the prediction varies as a function of variables of interest, by averaging over other variables.Not recommended if the features are correlated**

* **Accumulated Local Effects (ALE): describes how features affect a model prediction.It shares the same goal as PDP (Partial Dependence Plot).Overcomes the features correlation problem by averaging and accumulating the difference in predictions across the conditional distribution, limiting the effects of specific features.**









##### ReLU-DNN
##### loan_to_value_ratio_std
![PFIRELU](https://user-images.githubusercontent.com/111473895/244163945-c878131b-cd05-4288-960a-ce1e93a10cc0.png)
* **There is a negative relationship between ‘mortgage is high priced’ and ‘loan_to_value_ratio_std’ when the value is above 0. As ‘loan_to_value_ratio_std’ increases, the probability of that individual’s mortgage to be ‘high priced’ decreases. There is a hike at first because the relationship is positive if the value of ‘loan_to_value_ratio_std’ is less than 0.**


![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/46a63e44-91e8-4e89-a9ff-99991c2a16ff)
* **There is a positive relationship between ‘mortgage is high priced’ and ‘Debt_to_income_ratio_std’ when the value is less than 1. As ‘Debt_to_income_ratio_std’  increases, the probability of that individual’s mortgage to be ‘high priced’ increases, up until the ratio is at around 1, then the relationship is negative.**

![PFIRELU]((https://github.com/thebader9/RMLGROUP2/assets/111473895/28b7a939-a871-46a7-8bc9-f804adccf652)
* **There is a negative relationship between ‘mortgage is high priced’ and ‘Property_value_std’. As Property_value_std’ increases, the probability of that individual’s mortgage to be ‘high priced’ decreases.**


![PFIRELU](https://github.com/thebader9/RMLGROUP2/assets/111473895/4f1283aa-0047-49c9-947f-b57f97433997)
* **There is a negative relationship between ‘mortgage is high priced’ and loan_amount_std. As ‘loan_amount_std’ increases, the probability of that individual’s mortgage to be ‘high priced’ decreases.**











##### XGB2
![PFIXGB2](https://user-images.githubusercontent.com/111473895/244147475-4dbd54ca-7e0d-4e4f-8c8f-81323b6eed5c.png)

* **As seen in ALE there is a positive relationship between loan_to_value_ratio_std and high_priced_mortgage. As loan_to_value_ratio_std increases, the probability of that individual for getting high_priced_mortgage increases.However PDP is constant at certain points and this doesn’t have effect on behavior.**

![PFIXGB2](https://user-images.githubusercontent.com/111473895/244149016-205f4396-cd74-4610-8afe-949ce00598e0.png)
* **There is a negative relationship between property_value_std and high_priced_mortgage as seen in ALE.As loan_to_value_ratio_std increases,the probability of getting high_priced_mortgage decreases.**

![PFIXGB2](https://user-images.githubusercontent.com/111473895/244149147-94a77ca7-352c-444e-86cb-8c6949a2cf3f.png)
* **As seen in ALE there is a positive relationship between debt_to_income_ratio_std and high_priced_mortgage. As loan_to_value_ratio_std increases, the probability of getting high_priced_mortgage increases.In PDP however the probability of that individual’s mortgage to be ‘high priced’ increases, up until the ratio is of around 0.7, then the relationship is negative.**

![PFIXGB2](https://user-images.githubusercontent.com/111473895/244149288-14e2825a-b9c4-487a-87cd-7c0d0b17ad5d.png)
* **As seen in PDP the likelihood of a high priced mortgage goes up with increase loan amount and has positive relationship with loan amount. The feature in global explain ability ranks low compared to other features so the importance of this prediction in overall model predictability is low.**

![PFIXGB2](https://user-images.githubusercontent.com/111473895/244149480-80f6979c-c03a-4d2f-b57c-78bbb41596ca.png)
* **There is a negative relationship between ‘mortgage is high priced’ and income _std. As ‘income _std’ increases, the probability of that individual’s mortgage to be ‘high priced’ decreases.**

![PFIXGB2](https://user-images.githubusercontent.com/111473895/244149555-99592278-78ad-4d85-9469-169db4a661c9.png)
* **As seen in ALE the maximum probability of high priced mortgage is at the value of 0.1 of intro_rate_ period and then there is negative relationship.The feature in global explainability ranks low compared to other features so the importance of this prediction in overall model predictability is low.**

![PFIXGB2](https://user-images.githubusercontent.com/111473895/244149598-24ad36bb-1d52-4893-9433-e3a0191b1631.png)
* **The PDP graph suggest the ‘absence of an introductory rate period (1) ‘is associated with a slightly higher likelihood of a high-priced mortgage.However, in ALE the result are different where ‘ absence of introductory rate period (1)’ ) does not strongly influence the probability of a high-priced mortgage.**

![PFIXGB2](https://user-images.githubusercontent.com/111473895/244149643-f984ec2c-6ee9-4ba2-b391-67811c9d862c.png)
* **The PDP graph indicates that having a standard 360 month mortgage (1) is associated with a slightly higher likelihood of a high-priced mortgage, while the ALE graph shows that having a standard 360 month mortgage (1) does not strongly influence the probability of a high-priced mortgage.**

![PFIXGB2](https://user-images.githubusercontent.com/111473895/244149687-2c42f0ff-e398-4e39-a74b-fba77398de9a.png)
* **The PDP chart indicates that having a conforming mortgage (1) is associated with a higher likelihood of a high-priced mortgage, while in ALE it shows that having a conforming mortgage (1) is associated with least likelihood of getting a high priced mortgage as it is close to 0.**

![PFIXGB2](https://user-images.githubusercontent.com/111473895/244149714-d6efafe4-1786-48c8-bf29-d2b11659b720.png)
* **Both PDP and ALE represent that the presence of higher debt to income ratio(1) will lead to high priced mortgage.**
