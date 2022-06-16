# Virtual Machine (VM) Exercises

## :information_source: Read this before getting started
- The goal of exercises in case study is for learners to apply what was learned in the previous courses to new problems or situations. This is best pedagogical practice for retaining and building skills.
- We can only run free versions of BI software in our virtual machine exercises. In the case of Power BI, make sure the exercises can run on [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) without any additional paid products. 
- Unsure what the scope of an exercise should be? Here's an [example](https://campus.datacamp.com/courses/case-study-analyzing-customer-churn-in-tableau/exploratory-analysis-1?ex=4) from the Case Study: Analyzing Customer Churn in Tableau. The first chapter of most DataCamp courses are free, so take a look at our [BI courses](https://learn.datacamp.com/courses?technologies=Tableau&technologies=Power%20BI) to get a feel for how we assess and guide learners in **case studies**.

## 1st VM Exercise

#### Dataset

- [x] Add datasets used to the `datasets/` folder

#### Files

- [x] **Initial**: Add file to the `exercises/`  folder with the name `ex-1-intial.twbx` or `ex-1-intial.pbix`, depending if you are auditioning for a Tableau or Power BI course.
- [ ] **Solution**: Add file to the `exercises/`  folder with the name `ex-1-sol.twbx` or `ex-1-sol.pbix`

#### Learning Objective

*Calculating Inventory Turnover*

#### Context
JEPETO's STORE Management has gave you information about their inventory. You will calculate the `Cost of Goods Sold (COGS)`  and the `Inventory Turnover` of each item over a year to have a better idea of how fast items are being sold and to know the gross margin the company has made for the year.

We do not recommend doing so, but if you lost progress you can load the solution workbook of the previous exercise `ex-1-sol.pbix` from the workbook folder.


#### Steps to be executed by the student (max 6)

Exercise 2.3. Key inventory analysis metrics 

- Step 1

It seems there is information of 2 years. Create a visualization of the invoice date and the quantity of orders to explore in which year there are more orders.
Hint: You can use many visualizations, but a barcharts could help see the counts easily.

- Step 2

Create two new columns called `Quantity_2020` and `Quantity_2021` that calculate the quantity of orders by each item type for each year.
Compute the initial stock for 2021 in a new column `2021_initial_stock`.
Hint: your formula should look like for example: `Quantity_2020 = CALCULATE(SUM(___),FILTER(Orders, Stock[___]=Orders[___] && Orders[___]=2020))`,
Once you have `Quantity_2020`, you can calculate `2021_initial_stock` by using `Original_stock` 

- Step 3

Calculate an initial stock for 2021 and the Cost of Good Sold (COGS) based on this stock quantity. 
Hint: Remember, the company has completely allocated the COGS for a particular item in the `UnitPrice`. Use this variable and the calculated stock quantity to compute the COGS for that particular year.

- Step 4

Calculate a new variable called `Average_value_inventory` that gives the average between the total cost of initial stock and the total cost of ending stock, using `UnitPrice`
Hint: You can use `unitPrice` along with `Original_stock` and `2021_initial_stock` to compute this average.

- Step 5

Create a new column `Inventory_turnover_2021` that calculates the Inventory turnover for 2021.
Make two barcharts to display which item has the highest value.
Hint: * For this exercise, you can use `unit_price` along with `Original_stock` and `2021_initial_stock` to compute this average.
For the visualization, you can use the description of the items by the average or sum of inventory turnover.


#### Exercise question:
*This is a question presented to learners to check if the steps above were properly completed. It can be a multiple choice question or a question with a 1-3 word answer. It is often not possible to check if all the steps are completed, in this case; the priority is to check that the learner meets the learning objective.*

#### End goal:

*Add an image of the final visualization here.*

## Finalized Workbook

#### Files
You can upload your final workbook in the exercises folder as `ex-final-sol.twbx` or `ex-final-sol.pbix`.

#### Explanation & Description
Which answers will the learner be able to solve once building this? How does it fit in the bigger picture?

#### End goal:

*Add an image of the final visualization here.*
