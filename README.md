# Introduction

FIFA World Cup is a football match played between countries between the interval of 4 years. The first FIFA World Cup was played 13 July, 1930 hosted by Uruguay. A total of 21 tournaments has been played. This analysis was carried out to find out the trend of how countries has participated in the tournament and how their performance has been so far.

# Data Collection

The data was scrapped from Kaggle.

![image](https://user-images.githubusercontent.com/101842162/181673040-a6a983be-30f7-4a9f-8a6a-62bc24803fda.png)

This data had information of the World cup from 1930–2014, which prompted me to scrap another dataset to get a full grasp of the information for World cup 2018 which had in it a dataset which has the information of the winners of the world cup from 1930–2018. This data was also scrapped from Kaggle.

![image](https://user-images.githubusercontent.com/101842162/181673118-5231a2f4-9f32-42e8-a10e-58878874819b.png)

# Data Preparation

I created a folder where the datasets I worked with were kept, this was done to enhance easy navigation and accessibility.

![image](https://user-images.githubusercontent.com/101842162/181673202-8dd51abc-65f5-4c76-9e33-c6d5a3010916.png)

I then took a quick glance at the datasets in Microsoft Excel for the sake of understanding the structure of the data.

![image](https://user-images.githubusercontent.com/101842162/181673277-7b95c964-e20f-4b49-8c80-feb3c565b488.png)

The data above gives an information on the FIFA World Cup from 1930–2014.

![image](https://user-images.githubusercontent.com/101842162/181673357-a56f5592-b8cd-4c84-bf18-535e2450a5d7.png)

The data above gives an information on the FIFA World Cup tournament played in 2018.

![image](https://user-images.githubusercontent.com/101842162/181673416-632fa95f-c24d-4533-bc34-f9bc7496f48e.png)

The dataset above shows a list of countries that has won the World Cup tournament sine 1930–2018.

After going through the dataset in Microsoft Excel I moved to Microsoft Power BI where i carried out my analysis and visualization.

The following are some of the steps I followed;

* used the Get data function on the Home tab of Power BI to connect to the data in the folder

![image](https://user-images.githubusercontent.com/101842162/181673536-e1170fc3-7b8c-41cc-84f1-879ec0971f77.png)

The data is a CSV (Comma-separated values) file, so I clicked on Text/CSV and navigated to the World Cup data folder which I created in which I kept the datasets I used. I clicked on the dataset I worked with and clicked Open.

![image](https://user-images.githubusercontent.com/101842162/181673614-da037d7b-9e58-47d7-89b2-e596736870c8.png)

* after clicking open the Navigation page opened where there are options like Load, Transform Data, Cancel.

![image](https://user-images.githubusercontent.com/101842162/181673735-4498ffda-be27-4ff0-aef2-3db144eee456.png)
 
* It is advisable to click on Transform Data so as to preview and make corrections where necessary in the data before loading it to Power BI. By clicking on Transform Data it opens up the Power Query Editor where I cleaned the data.

![image](https://user-images.githubusercontent.com/101842162/181673849-381fa327-3915-4dd7-9953-72431965a29f.png)

The Power Query Editor may open up without the distribution information of this data like the visual above, you may want to turn it on by clicking on the view tab and tick Column distribution and Column Quality as seen below.

![image](https://user-images.githubusercontent.com/101842162/181673925-54cb0288-da99-47c7-8113-abbe5fc26502.png)

The essence of the Column distribution and Column quantity is that it helps take a deep look into the dataset, it helps to easily detect if there’s an error in a dataset and also show the uniqueness of the dataset.

* the next step is to import the 2018 dataset which is also a CSV file to the Power Query Editor. I simply clicked on New Source on the Home Tab of the Power Query Editor I then selected Text/CSV and clicked Connect.

![image](https://user-images.githubusercontent.com/101842162/181674053-c0cb9642-fa5b-45af-a9d3-c3025840fac0.png)

I navigated to the folder I kept the datasets I worked with. In the folder I selected the 2018 dataset and clicked Open.

![image](https://user-images.githubusercontent.com/101842162/181674203-aa50376f-bc0b-4892-aba4-06d931c47a7c.png)

The Navigator where I selected Ok to load the data to the Power Query Editor.

![image](https://user-images.githubusercontent.com/101842162/181674264-1b23c636-8a6c-4689-a7da-ab98234be9bf.png)

I simply clicked OK to load the data to Power Query Editor.

![image](https://user-images.githubusercontent.com/101842162/181674346-d8d43859-e206-4a0f-8a66-1a02ee639850.png)

Now I have two different datasets (1930–2014 datasets and 2018 dataset) to work. I checked to confirm that the columns in the two datasets are similar so that Appending the two datasets will work.

I appended the two Queries using the Append as new function on the Home Tab of the Query Editor.

![image](https://user-images.githubusercontent.com/101842162/181674428-6539431d-2c65-4bc9-ac60-9aa4a18fde9d.png)

I clicked on the two datasets I’d like to Append and clicked okay.

![image](https://user-images.githubusercontent.com/101842162/181674532-cef6f40d-abc4-4fa7-a692-961f0729ab11.png)

note: the Append function is used when trying to combine different rows while Merge is used when trying to combine Columns which is why I used the Append function.
I then cleaned the data by removing the columns not needed for the analysis like the Home team initials, Away team initials, Winning condition etc. I did this by holding down my control button and clicking on the Columns I want to delete, after which I right clicked and selected Remove Columns.

![image](https://user-images.githubusercontent.com/101842162/181674707-9988edb2-6c46-46a4-b893-2cb50f99e477.png)

* the next thing I did was to split the Datetime column using the Split column function which helped split the Date and the Time into two different columns.

![image](https://user-images.githubusercontent.com/101842162/181674790-8395b1c0-a0ce-4ed8-90b3-9212736896b7.png)

I used the Split by Delimiter where I was able to specify how we want the column to be split.

![image](https://user-images.githubusercontent.com/101842162/181674844-d3fb8ade-6c09-4260-a617-40eb4099c685.png)

Now that I have the Date and Time in different columns. I then renamed the column appropriately.

![image](https://user-images.githubusercontent.com/101842162/181674910-c061308f-a927-4d5f-adc3-6bec3ab76e67.png)

* some countries over the years have had their names changed and in order to have a unique dataset I changed the names to the name they go by now. An example is Zaire which is now known as Congo. I changed this name by using the Replace value function. I simply right clicked on the column where I want to use the Replace value function, I then selected Replace value which popped up the Replace Value page as seen below.

![image](https://user-images.githubusercontent.com/101842162/181675015-47c0fbda-c9b7-4273-a973-b6a84bfb6315.png)

* the next thing I did was to import the third dataset which contained the information of winner from 1930–2018. We simply used the Get data function to import the dataset into the Power Query Editor. In this dataset I also used the Replace Value function to update the names of some countries.

![image](https://user-images.githubusercontent.com/101842162/181675146-a8c68351-744b-4b77-a11a-9add4ca79a4e.png)

* after this I used the Close & Apply function in the Home Tab to load the data to Power BI for further Analysis and Visualization.

# Data Visualization

Now that I have a clean dataset I went ahead to visualize the data using charts thought appropriate. In the dashboard I used Cards to visualize information like Total Attendance across all the World Cups, Total goals recorded, No of Matches played, Number of World Cup winners etc.

![image](https://user-images.githubusercontent.com/101842162/181675246-1443483c-e6ec-4285-86cc-c8092dd6b1b6.png)

![image](https://user-images.githubusercontent.com/101842162/181675286-39fbbb06-5cc6-4892-8489-abc261258f93.png)

I used the line chart to visualize the match outcome of both Away and Home teams. In this we can easily tell the country with highest goal scored across the years. The year slicer can be applied to find out the match outcome per year.

![image](https://user-images.githubusercontent.com/101842162/181675361-44b044c1-7730-433b-a1a8-5f8aa882fa4b.png)

I then used the Stacked Column chart to visualize the Highest Average Attendance by Stadium where we can see the Stadium that had the highest attendance across the years. The year slicer can also be used to determine the stadium that had the highest attendance per year. The Visuals show that Maracanã stadium had the highest attendance.

![image](https://user-images.githubusercontent.com/101842162/181675410-c0590ac8-dcd0-4e74-8045-e243832e945a.png)

I then visualized the country with the highest goal scored over the years using the Stacked Column Chart. The year slicer can be applied to find out the highest goal scored by countries per year. Brazil had the highest goals scored with a total of 259 goals.

![image](https://user-images.githubusercontent.com/101842162/181675474-dee94c05-db70-417b-9246-3eeec5964f51.png)

I then visualized the country that had the most world cup winning title. Brazil has the highest winning title, they had won the title a total of 5 times.

![image](https://user-images.githubusercontent.com/101842162/181675528-3e2f8f8c-4a80-49bd-8fb6-470f4caebe71.png)

![image](https://user-images.githubusercontent.com/101842162/181675546-2f967aa7-7fe9-432a-b610-f3edca0b600b.png)

The number of goals scored by the Home and Away team were visualized separately using the Stacked Bar Chart. The year slicer can be used to determine how these teams performed over the years.

![image](https://user-images.githubusercontent.com/101842162/181675603-94072410-6bfb-4c91-b032-1a7527cc545b.png)

![image](https://user-images.githubusercontent.com/101842162/181675630-5782c68d-36d7-488e-aa1a-5ca8a63ac8b1.png)

I then visualized the Highest attendance by match using the Stacked Bar chart as well.

![image](https://user-images.githubusercontent.com/101842162/181675693-9c8ec672-963e-4ac3-b595-f68ea2f6f799.png)

Conclusion

The different charts used can be referred to as Tiles, a combination of these Tiles on the Power BI Canvass is known as the dashboard. The dashboard I created is shown below:

![image](https://user-images.githubusercontent.com/101842162/181675743-271d0a6c-3445-40b0-9ae9-7ea45d82865c.png)

You can further interact with the dashboard hosted on the Power BI service [Here](https://app.powerbi.com/Redirect?action=openreport&context=Annotate&ctid=66b3f0c2-8bc6-451e-9603-986f618ae682&pbi_source=mobile_android&groupObjectId=&appId=&reportObjectId=da5655ee-c5cc-4e44-ad87-bd41e106ae2b&reportPage=ReportSection&bookmarkGuid=167bf56c-a958-48d8-9e5a-45c527ce9655)

You can connect with me on [LinkedIn](http://www.linkedin.com/in/oluwatobiloba-fatodu) and follow me on [Medium](https://medium.com/@fatoduoluwatobiloba).
