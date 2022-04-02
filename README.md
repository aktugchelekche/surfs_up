# Surf Up 

# Overview of Project :

In this project, I will utilize SQLAlchemy and SQLite to create a weather analysis for a upcoming business in Oahu. I will provide with detailed statistics regarding Weather as well as Preceptation for month of June and December. 

# Purpose of Surf Up  :

Main purpose of this project is to come up with a strong data/statistical analysis that will convince the investor(s) who want ensure that this business is profitable and sustainable. Since both of surfing and ice cream businesses have similar weather expectations such as less rain and high temprature, investors like to see evidence that Oahu meets these conditions. After I run my analysis, we have sufficient evidence that Oahu is a perfect fit for this type of business according to data from 2010 thorugh 2017. 

# Analysis

The first step is to use <code> create engine </code> function to set up the ability to query a SQLite database. Then, I reflect myr existing database into a new model with <code>automap_base()</code> function. Reflecting a database into a new model essentially means to transfer the contents of the database into a different structure of data. 

Now, I can reflect  tables with <code> prepare()</code> function. By adding this code, I will reflect the schema of our SQLite tables into our code and create mappings. After saving references to each table, I used an SQLAlchemy Session to query the database.

Lastly, I created a query that will extract each data for month of December and June by usiung <code> extract </code> and convert those result to a dataframe so that I can captured statistics such as avarage temperature and precipitation . I also used Seaborn to plot these information to for clear demostratation.

# Results :


1- Statistics for June included Precipitation Data:
* Temperature
  * Average Tempurature   : 74.94 F
  * Max/Min Tempurature   : 85/64 F 




<p align="center">
<img src= "https://user-images.githubusercontent.com/98676400/161296712-45899e99-835d-415b-b2ce-35859e183e6a.PNG" alt="Image 1-Pivot Table" width="300" height="400" /><img src="https://user-images.githubusercontent.com/98676400/161164859-6c41b65d-1f91-4bfd-a7e1-6a12003f5b16.png" width="400" height="350" />
</p>

2- Statistics for December included Precipitation Data:

* Temperature
  * Average Tempurature   : 71.0 F
  * Max/Min Tempurature   : 83.0/56.0 F 


<p align="center">
<img src= "https://user-images.githubusercontent.com/98676400/161297044-d6f666ed-5a29-4aba-be0b-47963a19c10c.PNG" alt="Image 1-Pivot Table" width="300" height="400" /><img src="https://user-images.githubusercontent.com/98676400/161165351-f87bb80a-42b5-450a-9f01-d177dfd81026.png" width="400" height="350" />
</p>


# Summary

### Comparasion December and June Temperature :

* Temperatures are more spread out in December (std = 3.7) than in June (std = 3.3).
* June’s mean and median are 74.94 °F and 75.00 °F respectively.
* December’s mean and median are 71.04 °F and 71.0 °F respectively.
* Maximum temperature in December is 83 °F and in June 85 °F.
* Minimum temperature in December is 56 °F and in June 64 °F.

<p align="center">
<img alt="Screen Shot 2022-04-01 at 9 14 36 PM" src="https://user-images.githubusercontent.com/98676400/161361774-dc1ab4e0-8106-4181-9c32-5d0a12faffd2.png" width="450" height="350" />
</p>

We can conclude that there is not much difference in the weather within June and December this implies that we can expect mild and steady temperatures year-round. Mean and median – also known as 2nd quartile - are closely together, meaning that distribution of the data is not spread out. 

<p align="center">
<img alt="Screen Shot 2022-04-01 at 9 14 36 PM" src="https://user-images.githubusercontent.com/98676400/161165255-6f845213-7d3b-45ce-aac1-d4b19b71a21c.png"
width="450" height="350" />
</p>

In term of tempurature, Oahu, Hawaii carries similar weather condition similar to other cities known as surf cities. Chart above table is a great referance for surf cities from "weatherspark.com"

### Comparasion December and June Precipitation :

In addition to temperature data, rainfall is as important as temperature for surfing business so that I have included summary statistics for " Precipitation" . 

* Precipitation is more spread out in December (std = 0.5) than in June (std = 0.33).
* June’s mean and median are 0.13 inches and 0.02 inches respectively.
* December’s mean and median are 0.21 inches and 0.03 inches respectively.
* Maximum rainfall in December is 6.42 inches and 4.43 inches in June.
* Minimum rainfall in December is 0 inches and 0 inches in June.

* Precipitation in June
  * Average Precipitation   : 0.136360 inches
  * Max/Min Precipitation   : 4.430000/0 inches 
<p align="center">
<img width="194" alt="Screen Shot 2022-04-01 at 9 25 37 PM" src="https://user-images.githubusercontent.com/98676400/161362128-adb019c7-3f43-4f7e-a3d4-49939bd5bc97.png">
</p>



* Precipitation in December
  * Average Precipitation   : 0.22 inches
  * Max/Min Precipitation   : 6.42/0 inches 
<p align="center">
<img width="192" alt="Screen Shot 2022-04-01 at 9 25 48 PM" src="https://user-images.githubusercontent.com/98676400/161362136-808e9280-9b17-44b2-ad38-eff208d5a7a2.png">
</p>



![Average Monthly Rainfall in Surf City](https://user-images.githubusercontent.com/98676400/161165250-9dd87a5a-c927-4202-a578-77e11e262815.png)



