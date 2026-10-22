# video-game-data-analysis
Statistical analysis of video game trends using Python, hypothesis testing, regression modeling, and data visualization

# Video Game Data Analysis: Sales, Statistical Inference, and Predictive Modeling

## Project Overview

This project explores relationships between video game sales, console platforms, review scores, and resale prices using statistical analysis and machine learning techniques.

Using a dataset of over 1,000 video games released between 2004 and 2010, I conducted exploratory data analysis, statistical inference, and predictive modeling to investigate trends in the video game industry.

The project is divided into three sections, each focusing on a different research question and set of statistical methods.

## Dataset

This project uses a video game dataset provided as part of **STAT 207: Data Science Exploration** at the University of Illinois Urbana-Champaign.

The dataset contains information about video games released between 2004 and 2010, including:

- **Console:** Gaming platform
- **US Sales:** Video game sales in the United States
- **Review Score:** Game review ratings
- **Sequel:** Whether a game is part of a series
- **Used Price:** Resale price of a video game
- **Year Released:** Year the game was released
- **Genre:** Video game category

**Data Source:** Course-provided dataset, STAT 207, University of Illinois Urbana-Champaign.

The dataset is not included in this repository because it was provided for educational use.

## Tools and Technologies

- **Python:** Data analysis and statistical modeling
- **Pandas and NumPy:** Data cleaning, manipulation, and numerical analysis
- **Matplotlib and Seaborn:** Data visualization
- **Statistical Inference:** Confidence intervals and hypothesis testing
- **Linear Regression:** Modeling used video game prices
- **Logistic Regression:** Classifying games by used price

## Methodology

### Section 1: Console and US Sales Analysis

**Research Question:** How do US video game sales differ across console platforms?

I analyzed sales distributions across five consoles:

- Nintendo Wii
- Nintendo DS
- PlayStation 3
- Sony PSP
- Xbox 360

The analysis involved examining missing values and duplicates, calculating descriptive statistics, and creating boxplots and bar charts to compare console sales.

**Key Findings:**

- Nintendo Wii and Xbox 360 games generally achieved higher US sales in the dataset.
- Sony PSP and Nintendo DS games tended to have lower sales.
- Sales distributions were heavily right-skewed, with a small number of blockbuster games accounting for exceptionally high sales.
- Differences between mean and median sales highlighted variation in performance across consoles.

These findings suggest that console platform is associated with game sales, although other factors may also influence performance.

### Section 2: Statistical Inference on Sequels and Review Scores

**Research Questions:**

1. What proportion of video games released between 2004 and 2010 were sequels?
2. Is there evidence that the population mean review score is below 70?

I drew a random sample of 200 video games and used statistical inference to investigate these questions.

**Methods:**

- Random sampling
- Descriptive statistics
- Confidence interval estimation
- One-sample hypothesis testing

**Key Findings:**

- Constructed a 95% confidence interval of **43.5% to 57.5%** for the proportion of games classified as sequels.
- Conducted a hypothesis test involving the population mean review score.
- Obtained a p-value of **0.8036**.
- Failed to reject the null hypothesis at a 0.05 significance level, indicating insufficient evidence that the population mean review score was below 70.

The analysis demonstrated how statistical inference can be used to estimate population characteristics and evaluate claims using sample data.

### Section 3: Predicting Used Video Game Prices

**Research Question:** What factors are associated with used video game prices, and can these factors predict whether a game has a relatively high resale price?

I developed two predictive models using video game characteristics.

#### Model 1: Linear Regression

Developed a linear regression model to predict Used Price using:

- Review Score
- Year Released
- US Sales
- Console dummy variables

**Results:**

| Metric | Value |
|---|---|
| R² | 0.3165 |
| Test RMSE | $6.84 |

Review Score showed a statistically significant positive relationship with Used Price. A one-point increase in Review Score was associated with an approximately $0.10 increase in predicted Used Price, holding other variables constant.

However, the model explained only 31.65% of the variation in used prices, indicating limited predictive power.

#### Model 2: Logistic Regression

Developed a logistic regression model to classify whether a game's used price was above or below the dataset median.

The model used:

- Review Score
- US Sales
- Year Released

**Model Performance:**

| Metric | Value |
|---|---|
| Classification Accuracy | 76.55% |
| AUC | 0.7688 |
| Sensitivity | 53.28% |

The model achieved 76.55% classification accuracy and an AUC of 0.7688, demonstrating moderate ability to distinguish between high- and low-price games.

However, sensitivity was relatively low, indicating that the model failed to identify a substantial proportion of actual high-priced games.

## Key Takeaways

- Analyzed video game sales and performance across multiple console platforms.
- Applied statistical inference to estimate population characteristics and test hypotheses.
- Developed linear and logistic regression models to investigate used video game prices.
- Evaluated predictive performance using R², RMSE, accuracy, AUC, and sensitivity.
- Identified limitations in statistical models and considered factors that may influence their results.

## Limitations

Several limitations should be considered when interpreting the findings:

- The dataset focuses on video games released between 2004 and 2010, limiting generalizability to newer games.
- Statistical inference was conducted using a random sample of 200 games, introducing sampling variability.
- Regression models did not account for every factor that may influence resale prices, such as rarity, physical condition, or collector demand.
- The linear regression model had limited explanatory power, while the logistic regression model showed relatively low sensitivity.

## Future Improvements

Potential improvements include:

- Incorporating additional features such as game genre, publisher, and popularity.
- Testing alternative regression and classification algorithms.
- Applying cross-validation to evaluate model performance.
- Investigating trends across additional console generations and release periods.

## Project Files

- **Video Game Analysis Notebook:** Contains the exploratory analysis, statistical inference, visualizations, and regression modeling.
- **README.md:** Project overview, methodology, results, and documentation.

## Project Context

This project was originally developed as part of **STAT 207: Data Science Exploration** at the University of Illinois Urbana-Champaign.
