# Test Topic DM 1B 2023-2024 - RESIT

**Total: 40 points**  
*(Final version after deleting question 4: 34 points)*

---

## Q1: [4 points]  
Each question is worth **2 points max**, **1 point** if only one of the two correct answers is mentioned,  
**-1 point** for each wrong item chosen.

Consider a case study in which patients are at high risk of postoperative death after a hip fracture based on preoperative characteristics. Data is available from different hospitals on thousands of hip fracture patients. Typically, from each patient, several characteristics are known such as:

- Symptoms of dementia
- Age
- Living situation
- Risk of malnutrition
- Fracture type
- Hb level
- Mobility score in the pre-fracture situation
- Length of stay in the hospital after surgery
- Post-operative wound infections
- Survival after 30 days following hip fracture surgery

We are interested in predicting for each patient the probability of postoperative death within 30 days after hip fracture surgery with logistic regression based on preoperative characteristics to support the decision for surgical treatment compared to nonoperative treatment.

### **Q1a: What kind of problem is it?** *(Select all that apply)*  
- [ ] a supervised problem  
- [ ] an unsupervised problem  
- [ ] a classification problem  
- [ ] a regression problem  

### **Q1b: What might be the features (attributes/predictors)?** *(Select all that apply)*  
- [ ] the length of stay at the hospital after surgery  
- [ ] symptoms of dementia  
- [ ] age of the patient  
- [ ] type of surgery  

---

## Q2: [5 points]  
Assume you have a dataset that you randomly split into a **training** and **test dataset**. Fill in the blanks:

1. If you have a model that has been fit on the training dataset, the **training error** is expected to be **[Select: larger than / smaller than / similar to]** the test error.  
2. In case of **underfitting**, both the training and test error are **[Select: large / small]**.  
3. In case of **overfitting**, the training error is **[Select: larger / smaller]** than the test error.  
4. A model suffering from **underfitting** will most likely have **[Select: high bias / high variance]**.  
5. If you fit a model using **K-nearest neighbors**, which choice of parameter \( K \) will result in overfitting?  
   - [ ] \( K = 2 \)  
   - [ ] \( K = 10 \)  
   - [ ] \( K = 20 \)  

---

## Q3: [2 points]  
Assume you have a **fixed training dataset (and test dataset)** and you want to develop a classification model. By sequentially adding parameters to increase the flexibility of your classification model, you are more likely to observe: *(Select all that apply)*  

- [ ] A wider difference between train and test errors  
- [ ] A reduction in the difference between train and test errors  
- [ ] An increased or steady train error  
- [ ] A decrease in the train error  

---

## Q4: **[Deleted]**  

*(This question was removed as the text for the first question was missing.)*  

---

## Q5: [2 points]  
A client has a classification problem and asks you to develop a model based on their data. You decide to use **regularized logistic regression (lasso)** as a method and choose **accuracy** as the performance measure. The regularized logistic regression model has a **hyperparameter lambda** that needs tuning via **grid search**. You use **5-fold cross-validation** to optimize lambda.

What is the final model that you will deliver to the client?  

- [ ] The regularized logistic regression model based on the whole dataset with the average value of lambda over the five folds.  
- [ ] A regularized logistic regression model based on one of the folds (taken randomly).  
- [ ] A regularized logistic regression model based on the whole dataset which is tuned for hyperparameter lambda with grid search on the whole dataset.  

---

## Q6: [2 points]  
What performance measures are most useful for a classification model?  

- [ ] Accuracy, Sensitivity, RMSE (Root Mean Squared Error)  
- [ ] Precision, R², Sensitivity  
- [ ] Sensitivity, Precision, Accuracy  
- [ ] Accuracy, R², RMSE (Root Mean Squared Error)  

---

## Q7: [3 points]  
Suppose that the **regression equation** relating **systolic blood pressure** \( y \) (in mmHg), **age** \( x \) (in years), and **smoking** \( z \) (yes = 1, no = 0) is:

\[
y = 98 + 0.8 \cdot x + 5.0 \cdot z + 0.1 \cdot x \cdot z
\]

What is the **increase in systolic blood pressure** for a **one-year increase in age** for a **smoker**?  
*(Give your answer as a fraction with one decimal.)*  

---

## Q8: [16 points]  
You work at a **bank** and want to develop a classification model to determine whether clients **who borrow money** will **default** or **not**, based on these attributes:

- **X1**: Home Owner (**Yes / No**)  
- **X2**: Marital Status (**Single / Married / Divorced**)  
- **X3**: Annual Income (**High / Low**)  

You choose to use a **Naïve Bayes classifier** and a **Decision Tree**. Below is the given dataset:

| Client | Home Owner | Marital Status | Annual Income | Default |
|--------|-----------|---------------|--------------|---------|
| 1      | Yes       | Single        | High        | No      |
| 2      | No        | Married       | High        | No      |
| 3      | No        | Single        | Low         | No      |
| 4      | Yes       | Married       | High        | No      |
| 5      | No        | Divorced      | Low         | Yes     |
| 6      | No        | Married       | Low         | No      |
| 7      | Yes       | Divorced      | High        | No      |
| 8      | No        | Single        | Low         | Yes     |
| 9      | No        | Married       | Low         | No      |
| 10     | No        | Single        | Low         | Yes     |

**Conditional Probability Calculation (Naïve Bayes):**  

1. Compute \( P(X_1 = Yes | Default = No) \).  
2. Compute \( P(X_1 = No | Default = No) \).  

**Prediction Task:**  
A new client has the following attributes:  
- Home owner = **No**  
- Marital Status = **Divorced**  
- Annual Income = **Low**  

What is the probability that this client will **default**?  
*(Give your answer as a fraction with two decimals.)*  

**Decision Tree Questions:**  

1. Compute the **classification error rate** for the attribute **Marital Status**. *(Give your answer as a fraction with two decimals.)*  
2. What will be the **splitting attribute** in the top root of the Decision Tree using the **classification error rate**? *(Select one.)*  
3. Compute the **overall Gini index** for the attribute **Marital Status**. *(Give your answer as a fraction with two decimals.)*  

---

## End of Test
