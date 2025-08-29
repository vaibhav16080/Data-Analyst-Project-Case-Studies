# Data Analyst Project Case Studies

Welcome! This is my collection of data projects, where I use data to solve problems and help businesses grow.

My approach is simple: I start by understanding a real-world business challenge, then I dig into the data to find clear, practical insights. The goal is always to provide answers that lead to smarter decisions and better results.

### My Approach

* ** Strategic Thinking:** I map out a clear plan to tackle important business goals, whether it's understanding customer behavior, finding ways to be more efficient, or predicting future trends.

* ** Powerful Tools:** I use advanced SQL and Python to explore data, build predictive models, and uncover the answers that truly matter.

* ** Trustworthy Results:** I apply proven statistical methods to ensure my findings are solid and reliable, not just based on chance.

Each project here tells a story—from the initial question to the final solution. I invite you to see how I turn raw data into a powerful tool for success.




### **Project 1: Target Retail Data Analysis with Advanced SQL**

#### **Objective**
The primary objective of this project was to dissect Target's retail dataset to uncover actionable insights into **sales performance**, **customer purchasing patterns**, and **supply chain efficiency**. The goal was to translate raw transactional data into strategic recommendations for optimizing marketing spend, improving customer retention, and streamlining logistics.

---
#### **Methodology & Technical Implementation**
The analysis was performed entirely within a **SQL environment**, focusing on sophisticated data manipulation and aggregation to answer complex business questions.

* **Data Extraction & Transformation:**
    * Utilized **Common Table Expressions (CTEs)** to structure complex queries, breaking down the logic for calculating multi-step metrics like customer lifetime value and month-over-month growth.
    * Performed extensive data cleaning and standardization directly in SQL, using **`CASE`** statements to segment customer demographics and **`CAST`** functions to ensure data type consistency across joined tables.

* **Sales & Customer Behavior Analysis:**
    * Leveraged advanced **window functions** like **`RANK()`**, **`DENSE_RANK()`**, and **`ROW_NUMBER()`** to identify top-performing products within each category without self-joining.
    * Employed **`LAG()`** and **`LEAD()`** to perform time-series analysis, calculating Month-over-Month (MoM) order growth and comparing sales figures against previous periods.
    * Conducted a comprehensive **RFM (Recency, Frequency, Monetary) analysis** by segmenting customers into quartiles. This involved using subqueries and `GROUP BY` aggregations to calculate each customer's last purchase date (`DATEDIFF`), total number of orders, and total amount spent.

* **Performance & Logistics Optimization:**
    * Analyzed delivery performance by joining sales data with shipment tables, using **`AVG()`** and **`DATEDIFF()`** to calculate the average time-to-delivery across different regions and shipping carriers.
    * Calculated the **freight charge to sales ratio** for different product categories to identify areas where shipping costs were disproportionately high, potentially impacting profitability.

---
#### **Key Analytical Insights**
* **High-Value Customer Segment:** The RFM analysis revealed that the top **15%** of customers (high frequency, high monetary value) accounted for nearly **60% of total revenue**, highlighting a critical segment for targeted retention campaigns.
* **Profitability Drain:** Certain low-cost, bulky product categories showed a freight charge ratio exceeding **25%** of their sale price, indicating a significant drain on profit margins for those items.
* **Seasonal Demand Peaks:** Time-based aggregations showed a **35% spike** in electronics sales in the quarter leading up to the holiday season (Q4), suggesting a predictable trend for inventory planning and marketing.

---
#### **Actionable Recommendations & Business Impact**
* **Strategy:** Develop a **loyalty program** or exclusive offers for the identified high-value RFM segment to maximize customer lifetime value.
* **Operations:** **Renegotiate shipping contracts** for product categories with high freight costs or explore alternative logistics solutions like regional fulfillment centers.
* **Marketing:** **Reallocate marketing budget** to increase ad spend for the electronics category starting in late Q3 to capitalize on predictable seasonal demand.

***


### **Project 2: Netflix Content Strategy Analysis with Python**

#### **Objective**
This project aimed to analyze the Netflix dataset to understand its content library's composition, identify **global distribution patterns**, and **forecast future content demand**. The insights derived are intended to guide Netflix's strategic decisions on content acquisition, production focus, and market-specific library curation.

---
#### **Methodology & Technical Implementation**
This analysis leveraged a full suite of Python's data science libraries to move from raw data to predictive modeling.

* **Data Preprocessing & EDA:**
    * Utilized **Pandas** for robust data wrangling, handling missing values in columns like `director` and `cast` through imputation, and parsing complex date formats into datetime objects.
    * Used **NumPy** for efficient numerical computations required for statistical summaries.
    * Developed a comprehensive **exploratory data analysis (EDA)** using **Matplotlib** and **Seaborn** to visualize key trends. This included creating bar charts for top genres, count plots for content types (Movie vs. TV Show), and a choropleth map using **Plotly** to display the geographical distribution of content production.

* **Time-Series Forecasting:**
    * Engineered a time-series dataset by aggregating content releases by month and year.
    * Conducted a formal time-series analysis using **`statsmodels`**, decomposing the series into trend, seasonal, and residual components.
    * Developed and trained a **SARIMA (Seasonal AutoRegressive Integrated Moving Average)** model to forecast the volume of content releases for the next 12-18 months, validating the model's performance by checking for stationarity using the Augmented Dickey-Fuller test.

* **Predictive Modeling & Insights:**
    * Leveraged **Scikit-learn** to build a classification model to predict the genre of a title based on its description, providing a tool to automatically categorize new content.

---
#### **Key Analytical Insights**
* **Content Dominance:** The **United States** and **India** are the top two content-producing countries, but there is a rapidly growing trend of content acquisition from **South Korea** and **Spain**.
* **Genre Saturation:** While "Dramas" and "Comedies" are the most frequent genres, **"Documentaries"** and **"Stand-Up Comedy"** have shown the highest year-over-year growth in the last three years.
* **Forecasting Demand:** The SARIMA model forecasted a **20% increase** in the addition of TV Shows over Movies in the coming year, indicating a strategic shift towards episodic content.

---
#### **Actionable Recommendations & Business Impact**
* **Content Strategy:** **Increase investment** in acquiring and producing content from emerging markets like South Korea to diversify the content library and appeal to a global audience.
* **Production Focus:** **Allocate more production resources** to TV shows and high-growth genres like documentaries to align with viewer preferences and market trends.
* **Marketing:** Launch **targeted marketing campaigns** promoting region-specific content to enhance user engagement in international markets.

***


### **Project 3: Aerofit Customer Segmentation with Descriptive Statistics & Probability**

#### **Objective**
This analysis of the Aerofit dataset was aimed at creating **distinct customer profiles** for three different treadmill models. The goal was to understand the demographic, fitness, and income characteristics of typical buyers for each product, enabling the company to create highly targeted and effective marketing strategies.

---
#### **Methodology & Technical Implementation**
The project was grounded in statistical and probabilistic methods to move beyond simple averages and uncover the underlying relationships between customer attributes and product choice.

* **Descriptive Analytics & Statistical Profiling:**
    * Utilized **Pandas** to compute measures of central tendency (mean, median) and dispersion (standard deviation) for numerical features like age, income, and weekly usage.
    * Created two-way **contingency tables (crosstabs)** to analyze the relationship between categorical variables, such as treadmill model purchased versus marital status or gender.

* **Probabilistic Analysis:**
    * Calculated **Marginal Probabilities** to determine the overall probability of a random customer purchasing each treadmill model (e.g., $P(\text{Model KP281})$).
    * Calculated **Conditional Probabilities** to uncover deeper insights, such as the probability of a customer purchasing the high-end model given their self-rated fitness level is 5 out of 5 (e.g., $P(\text{Model KP781} | \text{Fitness} = 5)$). This provided a powerful lens for identifying key purchasing drivers.

* **Data Visualization:**
    * Used **Seaborn** and **Matplotlib** to create insightful visualizations, including stacked bar charts to show product preferences across income brackets and box plots to visualize the distribution of age for buyers of each model. These visuals were critical for communicating findings to non-technical stakeholders.

---
#### **Key Analytical Insights**
* **High-End Model Profile:** There is an **82% conditional probability** that a customer who self-rates their fitness as 4 or 5 will purchase the premium KP781 model. This segment also has a significantly higher average income.
* **Entry-Level Model Profile:** The entry-level KP281 model is the most popular choice, purchased by **40%** of all customers. Its buyers are evenly split between males and females and tend to have lower income and fitness levels.
* **Income as a Key Differentiator:** Customer **income is a stronger predictor** of treadmill model choice than age. A clear positive correlation exists between income level and the tier of the product purchased.

---
#### **Actionable Recommendations & Business Impact**
* **Targeted Marketing:** Design **separate marketing campaigns**: one focusing on performance and durability for the KP781 model targeted at fitness enthusiasts via gyms and health magazines, and another focusing on affordability and ease-of-use for the KP281 model targeted at beginners.
* **Product Bundling:** Since the mid-range KP481 model is popular among couples (based on marital status analysis), create a **"Partner Fitness" bundle** that includes a discount on a second product or service.
* **Sales Strategy:** **Equip the sales team with these profiles** so they can quickly identify customer needs and guide them to the most appropriate model, increasing conversion rates.

***


### **Project 4: Yulu Bike Rental Analysis with Hypothesis Testing**

#### **Objective**
This project involved a statistical analysis of the Yulu electric cycle rental dataset to identify the **key factors influencing rental demand**. By rigorously testing hypotheses, the goal was to provide data-backed evidence to help Yulu optimize bike allocation, manage inventory for seasonal demand, and make informed operational decisions.

---
#### **Methodology & Technical Implementation**
The core of this project was the application of formal statistical tests to validate assumptions about user behavior.

* **Exploratory Data Analysis & Assumption Checking:**
    * Initial EDA involved creating visualizations like box plots to compare rental counts across seasons and bar charts to see the effect of weather.
    * Before hypothesis testing, critical assumptions were validated. The **Shapiro-Wilk test** was used to check for normality of data distributions, and **Levene’s test** was applied to check for homogeneity of variances across different groups.

* **Hypothesis Formulation & Testing:**
    * Set a significance level ($\alpha = 0.05$) for all tests.
    * **ANOVA Test:** To determine if rental counts differ across seasons, a one-way Analysis of Variance (ANOVA) was conducted.
        * $H_0$ (Null Hypothesis): The mean rental count is the same across all four seasons.
        * $H_1$ (Alternative Hypothesis): At least one season has a different mean rental count.
    * **Chi-Square Test of Independence:** To assess if there is a relationship between the day of the week and weather conditions, this test was applied.
        * $H_0$: There is no association between the type of day (working vs. non-working) and the weather category.
        * $H_1$: There is an association between the type of day and the weather category.
    * **Two-Sample T-Test:** To compare the mean rental counts between working days and non-working days.
        * $H_0$: The mean rental count on working days is equal to the mean rental count on non-working days.
        * $H_1$: The mean rental count on working days is different from the mean rental count on non-working days.

---
#### **Key Statistical Findings**
* **Seasonal Impact:** The ANOVA test yielded a p-value well below 0.05, leading to the rejection of the null hypothesis. Post-hoc tests confirmed that rental counts in the **"Summer"** and **"Fall"** seasons are statistically significantly higher than in "Winter."
* **Weather's Influence:** The T-test comparing 'Clear' weather vs. 'Rainy/Cloudy' weather showed a significant difference, with far higher rentals on clear days ($p < 0.05$).
* **Working Day vs. Holiday:** The Two-Sample T-Test was statistically significant, indicating a discernible difference in rental patterns. Non-working days (weekends/holidays) showed higher average rental durations, while working days showed peaks during commute hours.

---
#### **Actionable Recommendations & Business Impact**
* **Dynamic Fleet Management:** Yulu should implement a dynamic fleet allocation strategy, **increasing the number of available bikes by 30-40%** during peak seasons (Summer/Fall) and deploying more bikes near parks and recreational areas on weekends.
* **Promotional Strategies:** Introduce a **"rainy day" discount** or a subscription model that is less weather-dependent to mitigate the drop in rentals during poor weather.
* **Demand Forecasting:** The validated factors (season, weather, working day) can now be used as **reliable features in a predictive machine learning model** to more accurately forecast daily rental demand.
