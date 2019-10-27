## MSDS6301 Case Study-01 - Beer Analysis

## Group members

This group project has two members: 

<a href="https://github.com/sachinac/smu_msds_6306/tree/master/msds_project_01"> 
Sachin Chavan </a><br>
<a href="https://github.com/Jsalsman7/SMU_MSDS"> Salsman Jordan</a>

## Purpose

To explore a dataset of breweries and beers, attempting to find something interesting in the data. The guiding questions and analysis process is shown in the analysis file. The presentations of this analysis are also provided.

## Description

The Beers dataset contains a list of 2410 US craft beers and Breweries dataset contains 558 US breweries.<br>
The datasets descriptions are as follows.

## Questions 

1.   How many breweries are present in each state?

2.   Merge beer data with the breweries data. Print the first 6 observations and the last six observations to check the merged file.  (RMD only, this does not need to be included in the presentation or the deck.)

3.   Address the missing values in each column.

4.   Compute the median alcohol content and international bitterness unit for each state. Plot a bar chart to compare.

5.   Which state has the maximum alcoholic (ABV) beer? Which state has the most bitter (IBU) beer?

6.   Comment on the summary statistics and distribution of the ABV variable.

7.   Is there an apparent relationship between the bitterness of the beer and its alcoholic content? Draw a scatter plot.  Make your best judgment of a relationship and EXPLAIN your answer.

8.  Budweiser would also like to investigate the difference with respect to IBU and ABV between IPAs (India Pale Ales) and other types of Ale (any beer with “Ale” in its name other than IPA).  You decide to use KNN classification to investigate this relationship.  Provide statistical evidence one way or the other. You can of course assume your audience is comfortable with percentages … KNN is very easy to understand conceptually.In addition, while you have decided to use KNN to investigate this relationship (KNN is required) you may also feel free to supplement your response to this question with any other methods or techniques you have learned.  Creativity and alternative solutions are always encouraged.  

9. Knock their socks off!  Find one other useful inference from the data that you feel Budweiser may be able to find value in.  You must convince them why it is important and back up your conviction with appropriate statistical evidence. 


## Analysis

### Presentation

* <a href="https://github.com/sachinac/smu_msds_6306/blob/master/msds_project_01/Sachin_Chavan_DDS_Case_Study01.pptx"> Powerpoint </a>
* Youtube Video

### Analysis Document

* <a href="https://github.com/sachinac/smu_msds_6306/blob/master/msds_project_01/Beers_Analysis.Rmd"> R Markdown Source</a>
* <a href="https://github.com/sachinac/smu_msds_6306/blob/master/msds_project_01/Beers_Analysis.html" target="_blank"> Knit Html file </a>
* Knit pdf output


### Datasets
* <a href="https://github.com/sachinac/smu_msds_6306/blob/master/msds_project_01/data/Beers.csv"> Beers.csv </a>
* <a href="https://github.com/sachinac/smu_msds_6306/blob/master/msds_project_01/data/Breweries.csv"> Breweries.csv </a> 
* <a href="https://github.com/sachinac/smu_msds_6306/blob/master/msds_project_01/data/state_abbreviations.csv"> state_abbreviations.csv </a>

## Codebook

Codebook Provides additional details about code and data.

**Beers.csv:**

|**Field Name** | **Description**                          |
|-------------|:-------------------------------------------|
|Name         | Name of the beer                           |
|Beer_ID      | Unique identifier of the beer              |
|ABV          | Alcohol by volume of the beer              |
|IBU          | International Bitterness Units of the beer |
|Brewery_ID   | Brewery id associated with the beer        |  
|Style        | Style of the beer                          |
|Ounces       | Ounces of beer                             |

**Breweries.csv:**


|**Field Name** | **Description**                          |
|---------------|:-----------------------------------------|
|Brew_ID        | Unique identifier of the brewery.        |  
|Name           | Name of the brewery.                     |
|City           | City where the brewery is located.       |
|State          |  U.S. State where the brewery is located.|

**Libraries:**

|**Library**    | **Purpose**                   |
|---------------|:------------------------------|
| ggplot2       | Visualizations                |  
| ggthemes      | Themes for ggplots            |  
| prettydoc     | Theme for RMD                 |  
| tidyverse     | Tidy data                     |  
| naniar        | Missing data Visualizations   |  
| visdat        | Missing data Visualizations   |  
| mice          | Imputations                   |  
| VIM           | Missing data patterns         |  
| stringr       | Strings processing            |           
| Hmisc         | for Capitalize function       |

**Variables in the Program:**

|**Variable Names** | **Purpose**                   |
|---------------|:---------------------------------|
| beers_ds      | Beers.csv                        |  
| breweries_ds  | Breweries.csv                    |  
| states_ds     | state_abbreviations.csv          |  
| bmerged_ds    | beers_ds+breweries_ds+states_ds  |  
| bmerged_ds    | beers_ds+breweries_ds+states_ds  |  
| bmerged_final_ds | After deleting missing data  |  
| model_ibu | regression model without transformation  |  
| model_log_ibu | regression model with transformation  |  
| imputed_df | final imputed dataframe derived from bmerged_final_ds  |  


**Program perfoms following steps:**

1. Load Beers.csv(beers_ds),Breweries.csv(breweries_ds) and state_abbreviations.csv(states_ds)
2. Remove Leading and trailing spaces in character variables
3. Merge Breweries.csv and state_abbreviations.csv by using State field into breweries_ds
4. Merge breweries_ds and beers_ds into bmerged_ds
5. Delete 62 records that have both values IBU and ABV missing
6. Create a regression model for imputation
7. Impute field IBU 
8. Perform analysis on this imputed data.

