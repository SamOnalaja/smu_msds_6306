# MSDS6306 Case Study-02 - Employee Attrition

# Group

This is an individual project.

# Purpose

DDSAnalytics is an analytics company that specializes in talent management solutions for Fortune 100 companies. Talent management is defined as the iterative process of developing and retaining employees. It may include workforce planning, employee training programs, identifying high-potential employees and reducing/preventing voluntary employee turnover (attrition). To gain a competitive edge over its competition, DDSAnalytics is planning to leverage data science for talent management. The executive leadership has identified predicting employee turnover as its first application of data science for talent management. Before the business green lights the project, they have tasked us to conduct an analysis of existing employee data. This R markdown does detailed statistical analysis of the given datasets and contains code,plots and all hypothesis test with conclusion. It also contains code and its output that was written to build predictive model as requested by talent management firm.

Along with this R code, we also built an app to perform EDA and interactive plots. We have posted this app on the web. 

Please visit the app on this link 
https://sachinac.shinyapps.io/msds_rshiny_cs02/

## Description

Goal 

1. Identify top 3 factors that lead to attrition
2. Job Role specific trends e.g data scientist have highest job satisfaction
3. Other insights if any
4. Build a model to predict attrition

## Analysis

### Presentation
* <a href="https://github.com/sachinac/smu_msds_6306/blob/master/msds_project_01/Sachin_Chavan_DDS_Case_Stu1.pptx"> Powerpoint </a>
* <a href="https://youtu.be/AdvavD-SqRU"> Youtube Video </a>


### Analysis Document

* <a href="https://github.com/sachinac/smu_msds_6306/blob/master/msds_project_01/Beers_Analysis.Rmd"> R Markdown Source</a>
* <a href="https://github.com/sachinac/smu_msds_6306/blob/master/msds_project_01/Beers_Analysis.html" target="_blank"> Knit Html file </a>

### Datasets
* <a href="https://github.com/sachinac/smu_msds_6306/blob/master/msds_project_02/data/CaseStudy2-data.csv"> CaseStudy2-data.csv </a>
* <a href="https://github.com/sachinac/smu_msds_6306/blob/master/msds_project_02/data/CaseStudy2CompSet%20No%20Attrition.csv">CaseStudy2CompSet No Attrition.csv	 </a> 
* <a href="https://github.com/sachinac/smu_msds_6306/blob/master/msds_project_02/data/CaseStudy2CompSet%20No%20Salary.xlsx"> CaseStudy2CompSet No Salary.xlsx </a>

## Codebook

Codebook Provides additional details about code and data.

CaseStudy2-data.csv

We can categorized fields as follows:


* **Non Predictors** 
  + ID 
  + EmployeeNumber
  + EmployeeCount
  + StandardHours
  + Over18<br>  

* **Nominal Categorical Predictors :**  
  + BusinessTravel
  + Department
  + EducationField
  + Gender
  + JobRole
  + MaritalStatus
  + OverTime<br>  

* **Ordinal Categorical Predictors :**
  + Education
  + EnvironmentSatisfaction
  + JobInvolvement
  + JobLevel
  + JobSatisfaction
  + PerformanceRating
  + RelationshipSatisfaction
  + StockOptionLevel
  + WorkLifeBalance<br>  

* **Numerical Predictors :**  
  + Age
  + DailyRate
  + DistanceFromHome
  + HourlyRate
  + MonthlyIncome
  + MonthlyRate
  + NumCompaniesWorked
  + PercentSalaryHike
  + TotalWorkingYears
  + TrainingTimesLastYear
  + YearsAtCompany
  + YearsInCurrentRole
  + YearsSinceLastPromotion
  + YearsWithCurrManager<br>  

* **Response Variable :**  
  + Attrition (for classification model)
  + MonthlyIncome (for regression model) <br>  
  
  
  **Program perfoms following steps:**
  1) Plot the data to analyze trend and inferences
  2) Run hypothesis test
  3) Build models
  4) Build R shiny app
   








