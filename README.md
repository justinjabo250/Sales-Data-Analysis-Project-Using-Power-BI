# Sales-Data-Analysis-Project-Using-Power-BI

My goal in this project is to use Power BI to perform a Sales Data Analysis project using a dataset provided by the company. This will allow me to explore and extract patterns and insightful, beneficial information that managers and stakeholders can use to enhance decision-making based on data analytics and take action to improve production and result in an amazing and encouraging increase in sales.

## I have listed the tasks that must be completed in order to reach our ultimate decision and the intended result of the preferred solutions here.

. Download Power BI [here](https://powerbi.microsoft.com/en-us/downloads/)
. After installing on your local computer, open Power BI. 


![1659324505788](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/a4a90eca-a476-4a00-805d-8941fbac930d)

#### Now it is time to begin our Analysis.

  . Under the **Home tab**, click on **Get Data**
  . Go to **Excel Workbook.** A new window will pop out for you to select your data.


![1659324647792](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/43943443-ac51-40cb-9489-e03360734314)

. Upload the data provided you and check **locations, people, products** and **sales** as shown in the picture below.


![1659324626834](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/8c0f3eda-89e7-4f04-b1a9-56e2faa4147c)


. Since our data is cleaned and is in the format that we want, there is no need to transform data. Click on **Load** at the bottom of the window.
. We return back to our Canvas. Next, we want to create a data model between the tables.
. Go to the left side and click on the third icon as shown in the picture below.


![1659324685194](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/e2751cda-8b19-47bd-91f3-2e4978081252)


. The data model view opens. You see that Power BI automatically connects people and products table to your sales table.
. In your **locations** table, drag **Geo** onto **Geography** in the **sales** table to create a relationship between the two table.


![1659324713678](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/e312bfe2-189e-4bd6-979d-ddbab893623d)


. We have created a **star schema** where our **sales** is the fact **table** and the other tables are the **dimension tables.**
. Go back to the **report view** i.e. The first icon on top of the model view icon.


![1659324736892](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/d839ed38-d4f5-4ac9-beeb-1234f6a0e628)


#### 1.Visualize Sales by location

   . Click on Stacked- Bar Chart
   . Drag Geo under location table to the X-axis
   . Drag Amount under the sales table to the Y-axis
   

![1659324759212](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/7056ad2b-acb2-476b-9b25-2459442b26bd)


#### 2.What is the company’s Total Sales?

    . Go to the sales table on the left side of the canvas
    . Right click on **Amount** and select **New measure**
    . Type the formula **Total Sales = sum(sales [Amount])** and hit enter



![1659324785806](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/5cee194a-7b3f-461e-8acc-66a1088699bf)


#### A new measure with name Total sales is created.


#### 3.What is our Total Cost as a company?

    . We don’t have the cost column in our tables, so we have to create a new column for our cost.
    . Go to the data view. The second icon under the report view at the far right of the canvas.
    . Go to **Table tools** at the top and click on **New Column.**


![1659324809518](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/90500b07-c916-41ef-bc4f-be509e6d66e0)

   . Type the formula **Cost = sales[Boxes] * RELATED(products [Cost per box])**

![1659324829057](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/8a5bbf28-b821-492c-b14b-7c87b45829db)

   . Hit Enter and return to the report view.
   . Now repeat the steps you used to create the Total Sales measure and create **Total Cost.** The formula for this is **Total Cost = sum(sales[Cost]).**
   
#### 4.What is the company’s Total Profit?

    . Again, create a **New measure** and name it **Total Profit**
    . Type the formula **Total Profit = [Total Sales] – [Total Cost]**
    . Create a New measure and name **it Profit%.** To calculate our **Profit%**, we divide **Total Profit** over **Total Sales.**
    . **Type Profit% = divide ([Total Profit], [Total Sales])**


#### 5.Has the Company met its Profit target?

  . Create a **New measure** and label it **Profit Target**
  . Type the formula **Profit Target Achieved? = if([Profit%] > 0.5, “Yes”, “No”)**


#### Time to start putting them all together on our canvas 😊

   . Go under **Visualizations** and select **cards**
   . Drag **Total Cost** and place in the fields box

![1659324857380](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/3f6817db-7f27-4cac-a272-6afdd63d9eed)

    . Go to **Format Visual**, the icon beside **Build Visual** under the **Visualization pane.**
    . Click on General and change the **Background color.** (Choose any color of your choice).
    . Turn on **Shadow** to give shadow effect to our card.
    . Click on the **Total Cost card** and press **CTRL + C.** Paste the visual by pressing **CTRL + V** in the canvas. Do those four times and align the cards as shown in the picture below.

![1659324891164](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/2c2e05db-d4f1-43b4-a335-55729981458b)


    . In the second card, change the field value from **Total Cost** to **Total Sales.**
    . For the third, change to **Total Profit** and the fourth to **Profit%**


![1659324916933](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/d4b209c8-d284-4267-9ac9-8711de9b3f51)


#### Now, we want to add currency sign to our values.

     . Click on the Total Cost measure on the right pane 
     . Go to Format and change General to Currency


![1659324936882](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/b0e45ac9-7f47-4b59-a7c1-166b4a7b2709)

  
    . Do same for the **Total Sales** and **Total Profit** Cards
    . Go to the Callout value and change the Font size to 50. Make it bold.
    . Do same for the remainder of the cards.
    

![1659324958357](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/a471c37e-160a-4db7-9d69-5d223ac32da0)


#### We want to see the trends of each metric over the months.

Click on an **Area Chart** under the **Visualization** pane.
Drag the **Month** column under the **Date Hierarchy** to the X-axis and drag the **Total Cost** to the Y-axis.



![1659324982409](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/54f5dbeb-d714-4e95-9d3f-df05e8377ff7)

    
    . Do same for the rest of the cards. **(Tip: You can use the copy and paste trick)**
    

![1659324997479](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/81209d0a-32f1-40f0-8c7b-4a29d9158f9c)


#### We want to see the performance of the Salespersons 

      . Click on **Table** under the Visualization pane
      . Add Salesperson, Total Profit, Profit% and Profit Target Acchieved? To the Values column
      . Add a conditional bar to the Total Profit column.
      . Go to **Total Profit** under the Values pane and click on the drop down.
      . Click on **Conditional formatting** and then **Data bars.**
      

![1659325070285](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/45355907-e817-4103-a61e-12cd4da3bb96)


#### We want to see performance of our products.

     . Repeat same steps for that of Salespersons

     
![1659325093589](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/929c0d6d-f6d2-46c4-b385-c272ff380d87)

#### Now bring back Sales per Country

![1659325114248](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/40f617f6-5db9-457a-877b-0abe74e9ea82)


    . Change the **Geo** to **Country.** To change the name, right click on the **X-axis** where you dropped the Geo data and select **Rename Visual.**
    . Change the title of the chart to **Total Sales by Country**
    . Add on more card and display the total number of **Customers**


![1659325133550](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/182e7fa2-52bf-4d6d-ad4e-709d496ef123)

#### Now we want to add title to our dashboard

    . Type a title of your choice. I am going for **Sales Dashboard Analysis**

![1659325158734](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/68d86091-dd52-482f-9b36-4b9faba522cb)

    . **Format the background color and style the font. Be creative😉**

![1659325181412](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/f88a9c8a-b57f-4f41-a3de-0296661dbb13)


#### Now we want to slice or filter our visuals 

      . **Add a slicer visual to the canvas and drag Teams under the people table to its values.**


![1659325204900](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/31d15eaa-b779-4203-92ab-a70bc57e9b3d)


    . Highlight the slicer chart and go to Format Visual, Visual and change the orientation from vertical to horizontal.
    . Change the background to suit that of title background i.e. Dark Blue
    . Press CTRL and left click on cards and area charts.
    . Right-click and group
    . Go to the insert bar and add a shape. Select rectangle and extend the shape to cover the cards and area charts.
    . Change the background color of the rectangle to white and go to format and send backwards



**You should end up with an output like this or even better. Be creative with your formatting.**



![1659325374390](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/5a37abae-c7b4-4d63-ad1a-7e113d3df918)


#### Share your Dashboard

     . **Log in with your azubi email by clicking on sign in at the top right corner.**


![1659325264050](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/3c1d58df-9017-460e-8145-e6a8937b154e)

    . **On the Home tab, click on publish and publish to your workspace.**

![1659325278309](https://github.com/justinjabo250/Sales-Data-Analysis-Project-Using-Power-BI/assets/115732734/09783781-19fa-4254-983e-fef3eb18e80c)

   . **Go to [Power BI service](https://app.powerbi.com/singleSignOn?ru=https%3A%2F%2Fapp.powerbi.com%2Fhome%3FnoSignUpCheck%3D1) and log in with your azubi email to view your dashboard and share to people as well.**



