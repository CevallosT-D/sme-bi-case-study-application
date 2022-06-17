# Virtual Machine (VM) Exercises

## :information_source: Read this before getting started
- The goal of exercises in case study is for learners to apply what was learned in the previous courses to new problems or situations. This is best pedagogical practice for retaining and building skills.
- We can only run free versions of BI software in our virtual machine exercises. In the case of Power BI, make sure the exercises can run on [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) without any additional paid products. 
- Unsure what the scope of an exercise should be? Here's an [example](https://campus.datacamp.com/courses/case-study-analyzing-customer-churn-in-tableau/exploratory-analysis-1?ex=4) from the Case Study: Analyzing Customer Churn in Tableau. The first chapter of most DataCamp courses are free, so take a look at our [BI courses](https://learn.datacamp.com/courses?technologies=Tableau&technologies=Power%20BI) to get a feel for how we assess and guide learners in **case studies**.


## 1st VM Exercise

#### Dataset

- [x] Add datasets used to the `datasets/` folder

#### Files

- [x] **Initial**: Add file to the `exercises/`  folder with the name `ex-1-intial.pbix`, depending if you are auditioning for a Tableau or Power BI course.
- [x] **Solution**: Add file to the `exercises/`  folder with the name `ex-1-sol.twbx` or `ex-1-sol.pbix`

#### Learning Objective

*Calculating Inventory Turnover*

#### Context
JEPETO's STORE Management has gave you information about their inventory. You will calculate the `Cost of Goods Sold (COGS)`  and the `Inventory Turnover` of each item over a year to have a better idea of how fast items are being sold and to know the gross margin the company has made for the year.

We do not recommend doing so, but if you lost progress you can load the solution workbook of the previous exercise `ex-1-sol.pbix` from the workbook folder.


#### Steps to be executed by the student (max 6)

Exercise 2.3. Key inventory analysis metrics 

- Step 1

It seems there is information of 2 years. Create a visualization of the invoice date and the quantity of orders to explore in which year there are more orders.

Hint: You can use many visualizations, but a barchart could help see the counts easily.

- Step 2

Go to the Stock table and create two new columns called `Quantity_2020` and `Quantity_2021` that use a DAX function with `CALCULATE()` to give the quantity of orders by each item type for each year.

Hint: your formula should look like for example: `Quantity_2020 = CALCULATE(SUM(___),FILTER(Orders, Stock[___]=Orders[___] && Orders[___]=2020))`.
 

- Step 3

Compute the Cost of Good Sold (COGS) based on 2021 stock quantity in a new column `COGS_2021`. Do not forget to change the format to currency.

Hint: 
Remember, the company has completely allocated the COGS for a particular item in the `UnitPrice`. Use this variable and the calculated stock quantity to compute the COGS for that particular year.

- Step 4

Calculate the initial stock for 2021 in a new column `2021_initial_stock` and use it to create a another variable called `Average_value_inventory` that gives the average between the total cost of initial stock and the total cost of ending stock, using `UnitPrice`. Make sure to keep the currency format.

Hint: Once you have `Quantity_2020`, you can calculate `2021_initial_stock` by using `Original_stock`.
You can use `unitPrice` along with `Original_stock` and `2021_initial_stock` to compute `Average_value_inventory`.

- Step 5

Now create another column `Inventory_turnover_2021` that calculates the Inventory turnover for 2021.
Make two barcharts, one that displays the Items by their Inventory turnover and another that shows the Items by the  which item has the highest value.

Hint: * For this exercise, you can use `unit_price` along with `Original_stock` and `2021_initial_stock` to compute this average.
For the visualization, you can use `Description` with the average or sum of `Inventory_turnover_2021`, and .
#### End goal:
![End_goal](https://github.com/CevallosT-D/files/blob/main/End_goal.jpg?raw=true)

#### Exercise question:
Does the Item with highest inventory turnover match the one with the highest quantity? Mention which is the item with the second highest inventory turnover.
Hint: Make sure that you correctly specified the quantity columns. Your formula should look like this: `Quantity_2020 = CALCULATE(SUM(Orders[Quantity]),FILTER(Orders, Stock[___]=Orders[___] && Orders[___]=2020))`; Where the first part of filter seeks a column that both tables have in common.
Feedback: Excellent! It seems Lip gloss is among the items that sell most often, perhaps JEPETO's STORE should include more items in a similar category.

## Finalized Workbook

#### Files
You can upload your final workbook in the exercises folder as `ex-final-sol.pbix`.

#### Explanation & Description
The learner gets to understand the concept of Inventory turnover and ABC Analysis whily in a practical way that allows him/her to find ways to calculate it given diferent data structures.

#### End goal - Dashboard temptative example:
![Dashboard](https://github.com/CevallosT-D/files/blob/main/Dashboard_ex.jpg?raw=true)
