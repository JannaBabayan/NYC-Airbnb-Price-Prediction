# New York City Airbnb Price Prediction Using Machine Learning

 Նախագծի նպատակն է New York քաղաքի Airbnb բնակարանների բազմաշերտ տվյալների հիման վրա կանխատեսել մեկ գիշերվա վարձակալության արժեքը:

##  Նախագծի Կառուցվածքը և Փուլերը

### 1. Exploratory Data Analysis (EDA) & Outlier Handling
* Տվյալների նախնական վիզուալիզացիայի (Scatter Plot & Boxplot) միջոցով հայտնաբերվել են էքստրեմալ մեծ արժեքներ (Outliers)` մինչև $10,000:
* Մոդելների ճշգրտությունը բարձրացնելու և աղմուկը հեռացնելու նպատակով իրականացվել է տվյալների ֆիլտրում՝ սահմանափակելով գների վերին շեմը **$1000**-ով:

### 2. Automated Pipeline & Preprocessing
Կոդի մաքրությունն ապահովելու և տվյալների արտահոսքը (*Data Leakage*) կանխելու համար օգտագործվել է Scikit-Learn-ի `Pipeline` և `ColumnTransformer`.
* **Թվային սյունակներ:** Լրացվել են միջին արժեքով (`SimpleImputer`) և մասշտաբավորվել (`StandardScaler`):
* **Կատեգորիկ սյունակներ:** Տեքստային տվյալները ձևափոխվել են թվային ձևաչափի (`OneHotEncoder):

### 3. Մոդելների Փորձարկում և Ուսուցում (Train-Test Split: 80/20)
Նախագծում իրար հետ համեմատվել են 7 տարբեր բարդության և տրամաբանության ալգորիթմներ.
1. `Linear Regression` 
2. `Lasso Regression`
3. `Uniform KNN` (KNN Regressor)
4. `Weighted KNN` (KNN Regressor)
5. `Decision Tree Regressor`
6. `Random Forest Regressor`
7. `XGBoost Regressor`



## Վերջնական Արդյունքներ և Մետրիկաներ
Մոդելների ճշգրտությունը և կանխատեսման որակը գնահատվել են ռեգրեսիայի հիմնարար չափանիշներով՝ **MAE**, **MSE** և **RMSE**:
