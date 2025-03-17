# Superstore Performance Insights

**Superstore Performance Insights** is a data analysis tool used to uncover key insights into sales, profitability, discount impact and shipping effiency. The project goal is to provide data-driven recommendations to optimise business strategies.

# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)


## Dataset Content
* Source: This was a public dataset I found on Kaggle (https://www.kaggle.com/datasets/vivek468/superstore-dataset-final/data)
* Key fields used: * Order Date, Ship Date for time based analysis.
                   * Sales, Profit and Discount to assess financial performance.
                   * Category and Sub-Category to assess performance of different product types.
                   * Ship mode, Region and State to monitor shipping effiency and geographical trends.

## How to Run the Analysis
1. Run 1_EDA.ipynd to explore summary stats and visualistions.
2. Run 2_DataCleaning.ipynd to check data for missing values, duplicates, remove unnecessary columns, etc. and to create the new csv file with the cleaned data.
3. Run 3_DataVisualistion.ipynb in order to visually and statisically validate the hypotheses outlined below.
4. Go to https://public.tableau.com/app/profile/conor.mcdevitt/viz/SuperstoreDashboard_17419641763650/SuperstorePerformanceDashboard and either download and run on Tableau desktop, or view it directly from the web. Click on various parts of the dashboard to interactively change the visualisations and filter them to display whatever information you would like in order to gain insights into trends by region, time etc.


## Hypothesis and how to validate?
1. "Higher discounts impact profitability negatively."
    In order to validate this hypothesis, I will be making scatter plots and box plots using the Discount and Profit columns to show this trend visually and I will also use statistical tests to confirm it mathematically.
    This hypothesis was confirmed when a significant negative correlation between discount levels and profit were found.
   
2. "Certain product categories are more profitable than others."
   For this hypothesis, I will use a bar chart to show profit by category and a boxplot to show profit distribution by category and then also use statistical tests to confirm this.
   This hypothesis was confirmed by showing that some categories tend to lead to higher profits, while others resulted in losses.

3. "Shipping mode and region affect delivery time."
   In this case, I will use boxplots for the distribution of delivery days with each shipping method and a heatmap to show the average delivery time by region, again, statistical tests will be use to confirm.
   This was partially confirmed by showing that shopping mode significantly impacts delivery time, although shipping region has minimal impact. Later in the interactive dashboard it could be seen that delivery time was significantly different, visually at least, when comparing states rather than just the regions themselves however.

4. "Larger orders (higher quantities) lead to higher total profits."
   For the final hypothesis, I will use a scatter plot showing profit vs quantity and a regression line chart to showcase the predictive relationship between quantity and profit. Statistical tests will be used to prove this.
   The final hypothesis was confirmed both visually as well as through the statistical tests showing that sales volume positively correlated with total profit.

## Project Plan
* A kanban board was utilised throughout the project in order to outline the steps I needed to take and to keep me on track to finish the project by the deadline (https://github.com/users/conormcdevitt/projects/4).
* Experience from previous hackathons was used in order to make up steps of the plan as well as how much time should be allocated to each step.
* The first stage after ideation and selecting a dataset involved data preparation and cleaning, which involved making two notebooks for EDA and data cleaning and the end result was a clean dataset which was ready for analysis, visualisation and the testing of hypotheses.
* Next up was another notebook to be used for more complex visualisations and statistical tests to prove the hypotheses that were outlined previously. Following this was where business recommendations/insights were included based on what was shown throughout the notebook.
* Finally, Tableau was used in order to create an interactive dashboard to gain actional insights into the dataset which would be easy to use and display data clearly.
* The readme file was updated at times throughout the project, but I planned to do the majority of the readme at the end when the rest of the project was finalised.

## The rationale to map the business requirements to the Data Visualisations
* Specific visualisation choices were made in order to directly map to key business requirements listed below, such as:
  1. Understanding overall sales and profit trends: The KPI summary and sales/profit overview would provide a snapshot of total sales and profitability for executives.
  2. Indentifying the impact of discounts on profitability: Discount vs Profit scatter plot and box plots were used to visualise how different discount levels affect profitability.
  3. Analysing sales and profit distribution across regions: A geographic map was used to highlight which states are most profitable and have the highest sales, as well as sales that are struggling in both aspects.
  4. Evaluating the efficiency of different shipping methods: Box plot of delivery time by shipping mode was used to show the variation of delivery time by shipping method.
  5. Identifying high/low performing product categories: A bar chart of profitability by product category was used to help decision makers decide which categories and sub-categories to focus on in order to increase sales or profits.
  6. Providing users with interactive analysis options: The dashboard used various charts as filters in order to get specific insights into profitability, sales, the effects of higher discount levels and how things vary from state to state. 
* This would allow decision makers to extract actional insights using these visualisations that are directly linked to business goals.

## Analysis techniques used
* Examples of Data analysis methods used and limitations explained with some alternative approaches:
  1. Descriptive statistics were used to summarise sales, profit and discount distributions. Outliers in sales and profit skewed the mean which reduced it's reliability.
  2. Outlier detection identified extreme values which would affect analysis, some high profit transactions could have been legitimate sales but were flagged and replaced in the dataset.
  3. Correlation analysis: Spearman and Kruskal-Wallis tests were used to test the relationship between certain categories, non-parametric tests were required due to the non-normal distributions of the categories.
  4. Visualistion techniques: Boxplots, scatter plots, bar charts and line charts were used to validate hypotheses in the Jupyter notebooks and to communicate findings interactively in the Tableau dashboard. Some charts in the notebooks were extremely cluttered, such as the scatter plots involving discount as its values were at fixed intervals.
* The analysis was structured into a few different phases:
  1. Exploratory Data Analysis (EDA) was performed to gain an insight into the structure of the dataset. Basic visualisations were used to understand the distribution of variables and the dataset was partially loaded in order to discover columns that could be removed in the data cleaning stage, it was also used to discover whether there were any duplicates or missing values in the dataset.
  2. Data cleaning was the next step that was performed, where using information obtained from the EDA, I removed unnecessary columns, converted some columns to the correct format(Ex. Order date, Ship date to datetime format), detected outliers and dealt with them accordingly and then created a new dataset with the clean data in order to prepare for more advanced visaulisations and hypothesis testing using statistical tests.
  3. Data visualisation and hypothesis testing was reading to be done after the data cleaning stage, where relevant visualisations to each hypothesis were made to either prove or disprove them visually, while statistical tests were performed to prove that there were correlations between certain columns and that these correlations were not down to chance.
* The dataset I used was a decent size so I did not find myself to be limited by it, only by filtering by specific states with low amounts of sales in the dashboard did I feel any sort of limitation with the dataset which made it harder to gain insights into those regions due to the lack of data provided.
* Gen AI tools such as chatgpt and co pilot were used in various ways throughout the project, they were used in the ideation phase in order to decide which charts/graphs should be used for the hypotheses I came up with. During the statistical testing step I used chatgpt to help with what testing methods to use, for certain variables none of the methods that had examples provided in the LMS seemed to work, so I was able to discover that the Spearman method (which was only briefly mentioned in one video) was best to use in a few cases in order to prove my hypotheses. Copilot would sometimes provide me with descriptions for the code I was writing, as well as predicting the remainder of the code I was writing which helped a lot in some cases where I was unsure of the exact syntax to use and would have had to go back to the LMS for examples. Copilot also helped fix lines of code where errors were preventing the code from executing. Chatgpt was also used while I was creating my dashboard in Tableau, in order to structure the layout better and also if I was having difficulties displaying the information I wanted, chatgpt would give step by step instructions on how to display said data.

## Ethical considerations
* Although this was a publically available dataset, I still removed personally identifiable information(customer names, postcodes) to protect privacy and ensure compliance with GDPR.

## Dashboard Design
* The Superstore Performance Dashboard contains 6 sheets providing interactive insights into the dataset:
  1. Sales and profit breakdown by region, by using a map of the states in the US and colour coding them based on the total sum of sales and also including the profit earned in each state, we are given insights into what states sold the most and which states were the most profitable.
  2. Overview of sales and profit, using a dual axis line chart, total profit and sales trends were shown month by month which highlighted times in the year were sales and profit were much higher than others, a forecast for the next year was also included.
  3. Profitability by Product Category, a bar chart was used to gain insight into which product categories and sub-categories were the most profitable and even showed that some sub-categories actually made a loss overall.
  4. Discount impact on Profitability, a line chart was used to to display the impact higher discounts had on each product category, showcasing the downward trend of profits as discount levels are increased.
  5. Delivery Time Distribution, a box plot was made to show the distribution of delivery times depending on which shipping mode was selected, highlighting which shipping mode should be selected in time sensitive cases.
  6. Key Performance Indicators, a table was made that displays some KPIs such as Sales, Profit, Avg. Discount, Avg. Delivery time and Quantity of items sold. 
* The dashboard was designed to effectively communicate complex data insights to different audiences, ensuring that both business decision-makers and data analysts can extract relevant insights easily. Key design principles include :
  1. A Clear and Intuitive Layout: A structured 2x3 grid layout allows for logical flow from high-level KPIs to detailed analysis.
                                   The first row focuses on key metrics and regional trends, while the second row breaks down product profitability and delivery time distribution.
  2. Interactivity for Deep-Dive Analysis: Filters and dashboard actions enable users to focus on specific regions, categories, and discount levels.
                                           Clicking on the map or category charts dynamically updates other charts, making insights more actionable.
  3. Tailored for Different Audiences: Executives & Managers: High-level KPIs and profitability trends for quick decision-making.
                                       Analysts & Data Teams: Detailed profitability breakdowns and regional performance to support strategic analysis.
  4. Consistent Visual Encoding: Diverging color scales help users quickly identify key trends.
                                 Boxplots and bar charts provide visual comparisons of key performance metrics.
  5. KPI Section for Quick Insights: The KPI panel at the top provides an at-a-glance summary of critical metrics like total sales, profit, discount,
                                     quantity of items sold and delivery performance.
                                     

## Future Work and Scalability
* If I had access to live data, it would be nice to automate bringing in new data to reflect real-time sales and profitability trends which would allow stakeholders to monitor business performance dynamically rather than relying on a one time analysis.
* I would like to create another notebook with predictive models included and create a dashboard using streamlit, where you could input certain values and receive a prediction of various KPIs, such as sales and profit based on other factors such as time of year or discount applied.
* Another possible future addition would be to create more pages on the dashboard utilising columns that ended up being unused in the cleaned dataset, such as profit margin or product IDs, which could provide deeper insights into the dataset.



## Main Data Analysis Libraries
* This project utilised several Python libraries for data cleaning, analysis and visualisation, these libraries were used primarily:
  1. Pandas: This was used for data manipulation(checking for null/missing values, removing columns, etc) and loading the dataset from a csv file.
  2. Matplotlib and Seaborn: These were used for static visualisations and EDA (Showed the distribution of the data in various columns before data cleaning).
  3. Plotly: This was used for more interactive visualisations, including scatter plots and bar charts, in order to prove/disprove the hypotheses that were outlined in the beginning of the project.
  4. Scipy stats and Penguoin: These were both used to statistically prove or disprove hypotheses in order to backup what the visualisations showed mathematically.


## Credits 

* In the data loading stage, I couldn't load the dataset initially due the encoding type of the file so I went through another person's project that was on kaggle that had it (https://www.kaggle.com/code/sasakitetsuya/data-analysis-for-marketing-strategy).
* Chatgpt was used throughout the project, helping with ideation, what statistical tests to use and also with the development of certain charts in Tableau, while copilot was used to fix errors in code, predictions in code helped with syntax and it also helped to explain the code at times.
* The LMS was used at times to see examples of code being used in order to implement it correctly in my project.


