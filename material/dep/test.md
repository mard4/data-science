# Data Science 202300200 – 2023/2024-1A  
**Test DEP – Oct 4th, 2023**  

- **Number of questions:** 12  
- **Total points:** 100  
- **Passing score:** 55  
- **Time:** 8:45 – 10:45  

---

## **Section: Concepts**

### **Q1: [4 pt]**  
What is a "foreign key"?  

- [ ] a) attribute(s) in a table that determine a logical group of records in a table  
- [ ] b) attribute(s) in a table that uniquely determine a record in a table  
- [ ] c) attribute(s) in a table that form a reference to the primary key of another table  
- [ ] d) artificially introduced code or number to function as a key  

### **Q2: [4 pt]**  
You obtain a source with data on buildings. You suspect that the attribute with the height of the buildings might contain typing errors. Which of the following statistics would be useful to calculate for this attribute?  

*(Select all that apply.)*  

- [ ] a) Correlation  
- [ ] b) Outliers  
- [ ] c) Histogram  
- [ ] d) Missings  
- [ ] e) Mean  

### **Q3: [6 pt]**  
Select all the reasons why domain understanding is important in the field of data analysis.  

- [ ] a) It allows for the use of statistical techniques without the risk of bias  
- [ ] b) It helps in identifying relevant variables and features for analysis  
- [ ] c) It allows for better data cleaning  
- [ ] d) It enables the creation of visually appealing data visualizations  
- [ ] e) It guarantees accurate predictive modeling results without the need for feature engineering  
- [ ] f) It assists in interpreting data patterns in context  
- [ ] g) It automates data cleaning and preprocessing tasks  
- [ ] h) It aids in formulating meaningful research questions  

### **Q4: [4 pt]**  
What is the technical term for the summarization of the characteristics of individual variables?  

- [ ] a) Data Imputation  
- [ ] b) Data Transformation  
- [ ] c) Data Segmentation  
- [ ] d) Data Profiling  
- [ ] e) Data Cleaning  
- [ ] f) Data Normalization  

### **Q5: [4 pt]**  
What is the primary purpose of data imputation?  

- [ ] a) To remove outliers from the dataset  
- [ ] b) To create new variables from existing ones  
- [ ] c) To standardize the data for modeling purposes  
- [ ] d) To fill in missing values in the dataset  
- [ ] e) To reduce the dimensionality of the dataset  

---

## **Section: Code Understanding (Python Version)**  

### **Q6: [6 pt]**  
For analyzing traffic patterns, an inlined logical design for a cube has been made in the form of a table. The table holds information on how many bikes, cars, and trucks pass by various points of particular roads. It also registers the speed of these vehicles.  

#### **a) For each attribute, determine whether it is a fact or dimension attribute.**  

| Attribute | Fact Attribute | Dimension Attribute |
|-----------|--------------|------------------|
| RoadID |  |  |
| Speed |  |  |
| Vehicle kind (bike, car, truck) |  |  |
| Day (day of the traffic measurement) |  |  |
| Count (how many vehicles passed by) |  |  |
| PointID |  |  |

#### **b) How many dimensions are there?**  
*(Write your answer in the space below.)*  

---

### **Q7: [6 pt]**  
Match the technical terms to the correct phase in the Data Science process.  

| Term | Data Preparation | Analysis | Use |
|------|----------------|----------|-----|
| Data transformation |  |  |  |
| Machine learning |  |  |  |
| Data cleaning |  |  |  |
| Decision making |  |  |  |
| Data mining |  |  |  |
| Deployment |  |  |  |
| Data exploration |  |  |  |
| Data visualization |  |  |  |

---


## **Section: Code Understanding – Python Version**  
*The test had two versions that were the same except for this "code understanding" section.*  
*The questions below are from the Python-version of the test.*

### **Q9: [a: 5 pt; b: 5 pt; c: 5 pt]**  
Given the following example Python code from the DEP course guide that constructs the 'product' dimension:

```python
product = data0[['Product_Name', 'Product_Category']]
product = product.rename(columns={'Product_Name': 'name', 'Product_Category': 'category'})
product = product.drop_duplicates(ignore_index=True, keep='last')
product['productid'] = product.reset_index().index
product = product[['productid', 'name', 'category']]
```

#### **a) What do the `[[` and `]]` brackets do in the first and last line?**  
*(Select the correct answer.)*  

- [ ] a. They omit the columns between the brackets from the variable on the left and leave the remaining columns.  
- [ ] b. They specify that a join should be performed between the two variables on the left using the columns between brackets for matching.  
- [ ] c. They convert the columns between brackets of the variable to the left into a data frame.  
- [ ] d. They check that the columns between brackets are present in the variable on the left; an error is produced if one or more are not present.  
- [ ] e. They select only the columns between the brackets from the variable on the left and omit the other columns.  

#### **b) What would happen differently if we used `"keep='first'"` instead of `"keep='last'"` in line 3?**  
*(Select the correct answer.)*  

- [ ] a. Although a duplicate means that two rows have the same attribute values suggesting that it doesn't matter which one is kept, the first one or the last one, the index numbering can be different after all five lines.  
- [ ] b. Nothing: a duplicate means two rows have the same attribute values, hence it doesn't matter which one is kept, the first one or the last one; and also the index number is the same because we reset the index in the fourth line.  
- [ ] c. A duplicate doesn't mean that the values of all attributes need to be the same, so keeping the first or last makes a difference for the attribute values.  

#### **c) Which of the following pieces of code result in a DataFrame?**  
*(Select all that apply.)*  

- [ ] a. `product`  
- [ ] b. `product['productid']`  
- [ ] c. `product.reset_index().index`  
- [ ] d. `data0`  
- [ ] e. `'Product_Name'`  
- [ ] f. `product[['productid', 'name', 'category']]`  

---

### **Q10: [a: 5 pt; b: 5 pt; c: 5 pt]**  
Given the following example Python code from the DEP course guide that joins the product dimension with the sales table:

```python
sales = pd.merge(sales, product, how='outer',
                 left_on=['Product_Name', 'Product_Category'],
                 right_on=['name', 'category'])
```

#### **a) What is the purpose of `left_on=['Product_Name','Product_Category']` and `right_on=['name','category']`?**  
*(Select the correct answer.)*  

- [ ] a. It appends the 'name' values of rows in the product table to the 'Product_Name' values in the sales table. 'category' and 'Product_Category' analogously.  
- [ ] b. It renames 'Product_Name' and 'Product_Category' in the sales table to 'name' and 'category'.  
- [ ] c. It specifies which attributes to use for the join: 'Product_Name' and 'Product_Category' from the 'sales' table and 'name' and 'category' from the 'product' table.  
- [ ] d. It specifies that 'Product_Name' is a naming attribute and that 'Product_Category' is a categorical attribute.  
- [ ] e. It specifies that lower/uppercase and anything before the '_' is irrelevant in comparisons, i.e., that 'Product_Name' is the same as 'name' and that 'Product_Category' is the same as 'category'.  

#### **b) What does `"how='outer'"` specify?**  
*(Select the correct answer.)*  

- [ ] a. It specifies that product names and categories are also a match if they match partially at the beginning or the end of the product names and categories.  
- [ ] b. It specifies that the join should be executed in full and not stop when an error occurs in the join process.  
- [ ] c. It specifies the join type to be 'outer join' as opposed to one of the other types of join like inner join, left join, right join, etc.  
- [ ] d. It specifies that the attributes on the outside are used for matching, i.e., the first attribute of sales and the last attribute of product.  

#### **c) What does `"pd.merge"` specify?**  
*(Select the correct answer.)*  

- [ ] a. It specifies that we select the "merge" attribute from the "pd" DataFrame.  
- [ ] b. It specifies that the "pd" and "merge" attributes of the "sales" DataFrame should not be affected by the join.  
- [ ] c. It specifies that we mean to execute the "merge" function from the "pd" package.  
- [ ] d. It specifies that the "pd" parameter of the join operation should be set to the value "merge".  


---

## **Section: Case**

### **Q13: [15 pt]**  
The management of a chain of car garages would like to optimize their processes regarding service and repairs. Their process is as follows:  
Customers reserve a timeslot (day) themselves with a garage in their vicinity. The reservation can be for a number of different kinds of requests like:  

- Changing tires  
- Repair of a dent  
- Thorough periodic check and service  
- Casual periodic check and service  
- Many more  

To keep an overview, these request kinds are divided into three categories:  

- Periodic service  
- One-off service  
- Damage repair  

The garage registers:  
- The moment of reservation  
- The moment when the car is delivered to the garage  
- The moment the request started  
- The moment the request is finished  
- The moment the customer picks up the car again  

For the optimization of this process, management would like to analyze:  
- The **waiting time** for the customer *(time between reservation and delivery of car)*  
- The **request duration** *(time between start and finish of request)*  
- The **parking time** *(time between delivery of car and start of request plus time between finish of request and pick-up)*  

Since the **car brand and type** (e.g., "Renault" is a car brand and "Renault Clio" is the car type) influences these times, management would also like to analyze which car brands and types have **higher waiting time and request duration**.  

They are also interested in **trends over time**, for example, to see that the request duration becomes lower in the period after a certain change in procedures.  
To determine the exact 'day of the request,' we take the moment of the start of the request as a basis.  

For each attribute, determine whether it is a **fact**, **lowest-level dimension attribute**, or a **higher-level dimension attribute**.  
You can also decide to **not include the attribute in the cube/star schema**.  

#### **Table of Fact and Dimension Attributes**  

| Attribute | Fact Attribute | Lowest-level Dimension Attribute | Higher-level Dimension Attribute | Not in Cube/Star Schema |
|-----------|---------------|--------------------------------|-------------------------------|-------------------------|
| Car type  |   |  |  |  |
| Datetime of car pick-up |  |  |  |  |
| Datetime of delivery of car |  |  |  |  |
| Request category (periodic service, one-off service, or damage repair) |  |  |  |  |
| Datetime of reservation |  |  |  |  |
| Customer |  |  |  |  |
| Datetime of request finish |  |  |  |  |
| Request duration |  |  |  |  |
| Datetime of request start |  |  |  |  |
| Request kind (i.e., tire change, dent repair, etc.) |  |  |  |  |
| Car brand |  |  |  |  |
| Waiting time for customer |  |  |  |  |
| Parking time |  |  |  |  |

---

### **Q14: [15 pt]**  
We collected data from a wide range of museums in The Netherlands containing information on paintings.  
Each museum sent a list with **one row per painting** in their collection.  
For each painting, they provide:  

- Name of the painter  
- Painting style  
- Year it was painted  
- The city where it was painted  
- The number of people on the painting  

The organization that collected this data asked you to analyze it.  

They are interested in **trends over time** concerning **how many people are on the paintings** (increasing or decreasing over certain time periods).  
They are also interested in comparing these trends **between painting styles** and **between the provinces where the paintings were painted**.  

**Task:**  
Provide a **conceptual design** for the cube for this data and questions in terms of a **star schema**.  

#### **Star Schema Design**  

- **Fact:**  
  - **Number of people on the paintings** *(3 points)*  

- **Dimensions:**  
  - **Year** *(4 points)*  
    - The source data only contains ‘year it was painted,’ so any granularity finer than this **cannot** be derived from this source data.  
  - **Painting style** *(4 points)*  
    - The painter itself is **not relevant** for the questions.  
    - ‘Painting style’ is considered a **grouping of ‘painter’**, so using ‘painter’ instead of ‘painting style’ is **incorrect granularity**.  
  - **Province** *(4 points)*  
    - Although **‘city’** is recorded in the source data, only **data on ‘province’ level** is needed for answering the questions.  

---

### **End of Test**
