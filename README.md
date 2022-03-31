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


1- Statistics for  June :
* Temperature
  * Average Tempurature   : 74.94 F
  * Max/Min Tempurature   : 85/64 F 

<img width="147" alt="Screen Shot 2022-03-31 at 6 15 49 PM" src="https://user-images.githubusercontent.com/98676400/161164623-aa14df4f-1a23-4b4f-973c-eb0a99978088.png">

* Precipitation
  * Average Precipitation   : 0.136360 inches
  * Max/Min Precipitation   : 4.430000/0 inches 

<img width="180" alt="Screen Shot 2022-03-31 at 6 13 48 PM" src="https://user-images.githubusercontent.com/98676400/161164408-02bab3c2-a971-42a3-82c7-ac34052c1e8a.png">

<img width="464" alt="Screen Shot 2022-03-31 at 6 18 33 PM" src="https://user-images.githubusercontent.com/98676400/161164859-6c41b65d-1f91-4bfd-a7e1-6a12003f5b16.png">

1- Statistics for December :

* Temperature
  * Average Tempurature   : 71.0 F
  * Max/Min Tempurature   : 83.0/56.0 F 
<img width="140" alt="Screen Shot 2022-03-31 at 6 19 43 PM" src="https://user-images.githubusercontent.com/98676400/161164981-b4f6fc45-c599-4a70-9436-f62accba5eda.png">


* Precipitation
  * Average Precipitation   : 0.22 inches
  * Max/Min Precipitation   : 6.42/0 inches 

<img width="197" alt="Screen Shot 2022-03-31 at 6 20 25 PM" src="https://user-images.githubusercontent.com/98676400/161165039-06cf08a2-e1d6-4662-a6f5-21961bba6042.png">

<img width="459" alt="Screen Shot 2022-03-31 at 6 23 52 PM" src="https://user-images.githubusercontent.com/98676400/161165351-f87bb80a-42b5-450a-9f01-d177dfd81026.png">


![Average High and Low Temperature in Surf City](https://user-images.githubusercontent.com/98676400/161165255-6f845213-7d3b-45ce-aac1-d4b19b71a21c.png)

![Average Monthly Rainfall in Surf City](https://user-images.githubusercontent.com/98676400/161165250-9dd87a5a-c927-4202-a578-77e11e262815.png)



