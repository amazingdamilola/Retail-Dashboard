title of project
#Summarized Retail Dashboard

Scope:
Retail dashboard visualizng the summary aimed at the overall picture of how the business is performing.
 

data sources:
Microsoft excel

Cleaning and visulization tool:
Power Query and Power Bi

Understanding the informations in the data source:
The dataset consist of three sheets;
i. Dim Tables
ii. Fact Table
iii. Aug Data

More insights about the sheets:
i. Dim Tables:
The Dim tables sheets has some look up tables that i were used to group the sales data.
for example on the datasets, the financial year in austrialia runs from july through to june.
so i classifed each dates into its financial year, financial quarter and its financial year month 
-there are also informations about postcodes so we can see what surbhub and state they relate to.
-i also have a table on the sheet that has the buyer for each catergory and the manager for each surbhub.

ii. Fact Table:
The dataset spans from January 2016 to July 2017


Importing into Powerbi to tranform, load and visualize:
I already converted each sheets to tables in excel and then i selected them upon loadinig to power bi.

Cleaning and visulization:
The tools used to clean and visualize the datasets are
-Power query for cleaning
-Power Bi for visualization

Cleaning:
-The first thing i did was to make sure all the data types are correctly set.
-The next thing i did was to add a new column to the sales table to calculate the Total sales and since we already have sales price, the cost price and the total units then i proceeded to add some columns.
the columns i added to the sales table using the custom column buttons are;
a. Sales = Sales Price * Total Units
b. Cost = Cost Price * Total Units
c. Gross profit= Sales - Cost
-The next thing is did was change the data type of the new columns to decimal numbers.
-Lastly on power query, i closed and apply to load into power bi.


Visulization:

Now that my datasets are loaded into Power bi, below are the things i did to vizualize my datasets.

1.Establising Relationships in the Data Model:
so power bi automatically created a one to many relationship between the sales,Managers and the Regions tables.(the * shows that it is a one to manay relationship).
However, power bi left out the Date table and didnt create a relationship between the date table and other tables.
so i Dragged the date field in the sales table to date in the dates table to create a relationship.
i also deselected the relationship between Regions and sales table because there was already  relationshio created through the Managers table to the Sales table.

2.Fixing the Summarize icon for Postcode fields and the Financial Year month:
To do this i did the following:
i.hovered to Table view
ii. select the table from my list:
for postcode i selected Region and then i clicked on the modelling tab and then change from summarize to do not summarize.
i did the same thing for the financial month in the date table.

3. Formating the gross profit, cost and sales:
i selected each aforementioned columns and then formatted them to currency and then removed decimal places.


Visulating the dataset:

1.the first visualization i did was the KPI of the sales figure over time.
i used the a kpi visual to do this and then i changed the display to millions.

2. the second visual i did was a chart that showed the sales by state broken down by chain.
i used a clustered column chart. the fields i used for this charts were sales over region and then broken down by chain.
the chain was in the legend field and the state in the axis and the sales in the value fields.

3. The third visual was sales and gross margin by financial year quaters.
so i clicked on the sales, gross profit and financial year quaters to get the charts done.
i changed this visual further by making my gross profit in a line visual.
i also changed the format for my lables to one decimal place.

4. i showed the breakdown of sales by chain with a pie chart

5. i used a map view to show how different states were performing visually.
i used the globe map visualization and i used state and sales against state for this visual.
Due to the ambiguity of the state information of my dataset, on the region table, i concatenated the state and country so that my map visual can be more specific
using the power pivot module, i added a new column and names it state, country and then worte a state, country = Regions(state)&, Australia"
i also gave it the category "PLACE'.
lastly for this type of chart i removed the state field and replace it with the newly created column (state,country)
Note: with the field map, higher density of colors indicates higher value.

6. i also visualized sales and catergory by chain using a Bar chart because of the long category names.
i sorted this visual by the largest category and sorted by sales i.e Mens is the largest seller.


7.i did a visual of sales and gross profit by category accross time using a bubble chart.
i created a measure to calucate the gross profit percentage by taking the sum of the gross profit divided by sum of sales.
i went ahead to format the gross percentage fields to one decimal place.
the gross profit represents the size of the bubble
the play axis had the financial quarter.
whe x axis had the gross profit percentage.

8. lastly, i created a slicer to enable filter the dashboard by state.


POWER BI PROJECT LINK:

https://app.powerbi.com/view?r=eyJrIjoiZjEyZThmMWUtMzJlMi00ODQxLTkxMWMtOTk1ZjlkYWVlODZhIiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9








