# Superstore Performance Insights

**Superstore Performance Insights** is a data analysis tool used to uncover key insights into sales, profitability, discount impact and shipping effiency. The project goal is to provide data-driven recommendations to optimise business strategies.

# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)


## Dataset Content
* Source: This was a public dataset I found on Kaggle (https://www.kaggle.com/datasets/vivek468/superstore-dataset-final/data)
* Key fields used: * Order Date, Ship Date for time based analysis.
                   * Sales, Profit and Discount to assess financial performance.
                   * Category and Sub-Category to assess performance of different product types.
                   * Ship mode, Region and State to monitor shipping effiency and geographical trends.

## Business Requirements
* Describe your business requirements


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

## Project Plan
* Outline the high-level steps taken for the analysis.
* How was the data managed throughout the collection, processing, analysis and interpretation steps?
* Why did you choose the research methodologies you used?

## The rationale to map the business requirements to the Data Visualisations
* List your business requirements and a rationale to map them to the Data Visualisations

## Analysis techniques used
* List the data analysis methods used and explain limitations or alternative approaches.
* How did you structure the data analysis techniques. Justify your response.
* Did the data limit you, and did you use an alternative approach to meet these challenges?
* How did you use generative AI tools to help with ideation, design thinking and code optimisation?

## Ethical considerations
* Were there any data privacy, bias or fairness issues with the data?
* How did you overcome any legal or societal issues?

## Dashboard Design
* List all dashboard pages and their content, either blocks of information or widgets, like buttons, checkboxes, images, or any other item that your dashboard library supports.
* Later, during the project development, you may revisit your dashboard plan to update a given feature (for example, at the beginning of the project you were confident you would use a given plot to display an insight but subsequently you used another plot type).
* How were data insights communicated to technical and non-technical audiences?
* Explain how the dashboard was designed to communicate complex data insights to different audiences. 

## Unfixed Bugs
* Please mention unfixed bugs and why they were not fixed. This section should include shortcomings of the frameworks or technologies used. Although time can be a significant variable to consider, paucity of time and difficulty understanding implementation are not valid reasons to leave bugs unfixed.
* Did you recognise gaps in your knowledge, and how did you address them?
* If applicable, include evidence of feedback received (from peers or instructors) and how it improved your approach or understanding.

## Development Roadmap
* What challenges did you face, and what strategies were used to overcome these challenges?
* What new skills or tools do you plan to learn next based on your project experience? 

## Deployment
### Heroku

* The App live link is: https://YOUR_APP_NAME.herokuapp.com/ 
* Set the runtime.txt Python version to a [Heroku-20](https://devcenter.heroku.com/articles/python-support#supported-runtimes) stack currently supported version.
* The project was deployed to Heroku using the following steps.

1. Log in to Heroku and create an App
2. From the Deploy tab, select GitHub as the deployment method.
3. Select your repository name and click Search. Once it is found, click Connect.
4. Select the branch you want to deploy, then click Deploy Branch.
5. The deployment process should happen smoothly if all deployment files are fully functional. Click now the button Open App on the top of the page to access your App.
6. If the slug size is too large then add large files not required for the app to the .slugignore file.


## Main Data Analysis Libraries
* Here you should list the libraries you used in the project and provide an example(s) of how you used these libraries.


## Credits 

* In this section, you need to reference where you got your content, media and extra help from. It is common practice to use code from other repositories and tutorials, however, it is important to be very specific about these sources to avoid plagiarism. 
* You can break the credits section up into Content and Media, depending on what you have included in your project. 

### Content 

- The text for the Home page was taken from Wikipedia Article A
- Instructions on how to implement form validation on the Sign-Up page was taken from [Specific YouTube Tutorial](https://www.youtube.com/)
- The icons in the footer were taken from [Font Awesome](https://fontawesome.com/)

### Media

- The photos used on the home and sign-up page are from This Open-Source site
- The images used for the gallery page were taken from this other open-source site



## Acknowledgements (optional)
* Thank the people who provided support through this project.