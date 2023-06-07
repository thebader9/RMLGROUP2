# Responsible Machine Learning - Post hoc explainability

## Q1) Global Explainability and Interpretability

#### Permutation Feature Importance (PFI)
* **Permutation Feature Importance (PFI): Computes the change in prediction performance as the measure of feature importance. Breaks the relationship between the feature and the target, thus the drop in the model score is indicative of how much the model depends on the feature

##### EBM
** (Picture EBM PFI)
* **‘loan_to_value_ratio_std’ is the most influential feature in this model**
* **‘Property_value_std’, ‘Debt_to_income_ratio_std’, ‘loan_amount _std’ have a significant impact on the target variable (high priced)**

##### ReLU-DNN
** (Picture Relu PFI)
* **‘Property Value’ is the most influential feature in this model**
* **‘Loan to value ratio’, ‘loan amount’, ‘debt to income ratio’ have a significant impact on the target variable (high priced)**

##### XGB2

** (Picture XGPT2 PFI)
* **Loan_to _value _ratio_ std, Property value std and debt to income ratio std are the top three features that play pivotal role in deciding high_priced_mortagage among other features.**
