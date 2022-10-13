# Data-Visualliation.Neurons

The overview section produces the following output:

Automated Exploratory Data analysis with Pandas Profiling
To install the Pandas Profiling library, use this command:

!pip install -U pandas-profiling

We will use Pandas Profiling to generate a profile report. The report will give the dataset overview and dataset variables.

We generate the profile report using this code:

profile = ProfileReport(df, title='Pandas profile report', html={'style':{'full width':True}})
profile

The title of the generated report will be Data Visuallization Report. The profile report will have the following sections:

1.Overview

The overview section produces the following output:
![image](https://user-images.githubusercontent.com/108016928/195483278-d6fef901-ece0-4dab-a8ac-71fc62e7e67f.png)

From the generated report, the dataset has 4 variables and 111 observations/data points. The dataset has no missing values and duplication rows. The image also shows the variable types, which are categorical (2), Datetime (1), and numerical (1).

2.Variables

This section shows all the dataset variables. In addition, it provides useful characteristics and information about the variables.

The outputs below show some of the important variables:

DATE ,DESCRIPTION

![image](https://user-images.githubusercontent.com/108016928/195483675-b723daea-6b53-437d-8d40-cdbbc31c6ee4.png)

UNIT,PLACE

![image](https://user-images.githubusercontent.com/108016928/195483854-f7a4dbdd-bf63-47f3-85a3-72d04b57c50c.png)

3.Interactions

The interaction section has the following output:

![image](https://user-images.githubusercontent.com/108016928/195483992-07133358-e7b7-40cd-ac25-68b1a5401651.png)

4.Correlations
The correlation section shows the relationship between the dataset variables using Seaborn’s heatmap. Pandas Profiling allows toggling between the four main correlations plots.

These plots are the Phik (φk), Kendall’s τ, Spearman’s ρ, and Pearson’s r.

The correlations section produces the following output:

![image](https://user-images.githubusercontent.com/108016928/195486057-76dea40b-dadd-4c8c-8dde-03aba031bfcb.png)

Phik (φk)
Phik (φk) is a new and practical correlation coefficient that works consistently between categorical, ordinal and interval variables, captures non-linear dependency and reverts to the Pearson correlation coefficient in case of a bivariate normal input distribution. There is extensive documentation available here.

The image above shows the Phik (φk) correlation plot. We can easily toggle between the four main correlations plots to view the plots. By clicking the Toggle correlations descriptions button, we will view a detailed description of each correlation plot.

5.Missing values
This section shows if there are missing values in the dataset.

![image](https://user-images.githubusercontent.com/108016928/195486505-bf05a951-dede-475b-8f83-245c99cece3e.png)

The image shows the number of data points in each variable. All the variables have the same number of data points (111), except PLACE variable. It shows there are (103) missing values in the dataset.

Sample
This section displays the first 10 rows and the last 10 rows of our dataset.

6.First 10 rows

![image](https://user-images.githubusercontent.com/108016928/195486972-2bc7e496-874d-4a13-b6ff-ce4ff1497211.png)

7.Last 10 rows

![image](https://user-images.githubusercontent.com/108016928/195487676-769e40ae-0d63-42c9-8817-7bafd026b630.png)

8.Duplicate rows

![image](https://user-images.githubusercontent.com/108016928/195487737-4e03b6b3-d3bc-4de1-9b54-f1cbca7e4aea.png)

This marks the end of automated Exploratory Data Analysis using the Pandas Profiling. The library provides a descriptive analysis of our dataset and better understands the Data Visuallization dataset

9.Correlation Heatmap of UNIT variable

![image](https://user-images.githubusercontent.com/108016928/195488439-5be077db-9a00-4322-9f35-5f26e4acde8f.png)

10.Scatterplot between DESCRIPTION and PLACE Column

![image](https://user-images.githubusercontent.com/108016928/195489644-a907b40a-0f3d-49a9-84c2-286d7fea0182.png)

11.Histplot of Description

![image](https://user-images.githubusercontent.com/108016928/195489965-b569f76e-1036-4b99-a271-7643b5343428.png)

It shows Description variable is not normally distributed.And Beefs and Prawns are highest selling product.

12.Histplot of Place Variable 

![image](https://user-images.githubusercontent.com/108016928/195490780-5ffddbe6-e8ca-4715-83c0-163e88ff9475.png)

It shows Place variable is not normally distributed.Mallapuram is city where highest sell is done. 

13.Histplot of Place Variable 

![image](https://user-images.githubusercontent.com/108016928/195491326-7caf3cf5-b479-4b87-a9b0-6609b7b15601.png)

On date 15/04/2022 and 15/05/2022 highest sell is done.Date column is not normally distributed.

Conclusion

- Dataset has 5 (4.5%) duplicate rows Duplicates

- DATE is highly correlated with UNIT and place High correlation

- UNIT is highly correlated with DATE and place High correlation

- PLACE is highly correlated with DATE and unit High correlation

- PLACE has 8 (7.2%) missing values

Dataset statistics:

- Number of variables 4
- Number of observations 111
- Missing cells 8
- Duplicate rows 5

What can be done?

- Need to remove missing values.
- Need to remove duplicate rows.










