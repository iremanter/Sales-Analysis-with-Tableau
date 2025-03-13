# SALES ANALYSIS

“Online Sales Dataset”, includes seventeen attributes, which are as follows:

- InvoiceNo: A unique identifier for each transaction.
● StockCode: A unique code assigned to each product.
● Description: A description of the product.
● Quantity: The number of units sold.
● InvoiceDate: The date and time when the transaction occurred.
● UnitPrice: The price per unit of the product.
● CustomerID: A unique identifier for each customer.
● Country: The country where the transaction took place.
● Discount: The discount applied to the transaction.
● PaymentMethod: The method used for payment (e.g., Bank Transfer, PayPal).
● ShippingCost: The cost incurred for shipping the product.
● Category: The product category (Apparel, Electronics, Accessories, Furniture, Stationery).
● SalesChannel: The channel of sales which indicates whether the sales occurred online or
in-store.
● ReturnStatus: Indicates whether the product was returned or not.
● ShipmentProvider: The courier service handling the shipment (DHL, FedEx, Royal Mail, UPS)
● WarehouseLocation: The location from which the product was shipped.
● OrderPriority: The priority level assigned to the order (Low, Medium, High).

Key Performance Indicators (KPIs) has been defined. Calculated fields, sets, parameters, dynamic measures, and filters have been created using relevant formulas by using Tableau. 

The additional attributes are described in detail below:

● date: Extracts the date from the Invoice Date field.
● Customer_ID_fixed: Cleans the Customer ID field by removing dots.
● distinct_customer: Counts the number of distinct customers.
● Category2: Assigns a new category to products based on their description.
● Returned Count: Counts the number of returned items.
● Units Sold: Calculates the total units sold by excluding returned items.
● Revenue: Computes revenue by considering unit price, quantity sold, and discount.
● Profit: Calculates profit by subtracting shipping costs from revenue.
● Average Price: Computes the average price per unit sold.
● Total Profit By Year: Calculates the total profit for each year.
● Profit_Country: Computes the average profit per country.
● Cumulative Percentage: Calculates the cumulative percentage of quantities sold.
● Aggre-Level Overall Margin: Computes the overall profit margin at an aggregate level.
● High Margin?: Classifies margins as above or below average based on a threshold.
● revenue per dist customer: Calculates the revenue per distinct customer.
● Exclude Revenue LOD: Computes revenue while excluding a specific description.
● Measure Dynamic: Dynamically selects between revenue and quantity based on user input.

The detail explanation of the parameters and sets as follows:

● Top X Products by Quantity Sold: The top X products are determined based on quantity sold, with the selectable range between 1 and 11.
● Select Measure Name: Enables the user to choose between quantity or revenue as the measure to analyze.
● EU Set: A predefined selection of European countries.
● Description Set 2: Allows the user to select a number between 1 and 11 to display the top X
products in descending order based on quantity sold.

Dashbord 1: Country Analysis

The Country Analysis Dashboard with detailed explanation, some business insights and strategy recommendations are below:

The first visual, “Product Sold by Country (Not Returned)”, shows the relevant sales countries with different colors on the world map. By considering the amount of product sold, returned items are excluded to see the actual amount sold.

In the second chart, “Retailer Country Wise Financial Performance”, colored circles represent average profit amounts of each EU Country. In order to analyze only EU Countries, the EU set has been created before and then added to the filter area by creating this chart. It is shown that there is a slight difference between EU countries in terms of average profit. Therefore, strategic action to increase the profit can be applied equally to all countries.

In the third chart, “Return Rate Across Countries”, return rates have been calculated and it revealed that the highest return rate belongs to the Netherlands. The shipping cost can be increased a little to decrease the number of return items. Moreover, the survey can be hold with the customer who returned the items to understand the main reasons behind it.

The fourth chart, “Order Priority Across Countries”, shows both quantity sold and revenue of each country by selecting these measures from the Measure Dynamic. The colors shows whether the purchase happened in store or online. The United Kingdom and France show a slightly higher share of online orders, while Australia and Italy have more in-store orders.

In the last chart, “Margin Analysis by Product Category in Countries”, x-axis has been divided by EU Countries, and each country divided into products. Y-axis represents the computed profit margin at an aggregate level and the values range from 0 to slightly above 1, showing relative profitability. While blue bars indicate products with an overall margin at or below the threshold, orange bars highlight products with a higher-than-average margin within each country. This classification helps determine which product categories are performing better in terms of profit. Most product categories maintain a similar profit margin across countries. Some products, such as USB Cables and White Mugs, appear in orange, indicating higher margins in those categories for certain countries. The chart enables to identify profitable products per country and supports decision making in sales strategies, price adjustments, and inventory prioritization.

Dashboard 2: Product Analysis

The Product Analysis Dashboard with detailed explanation, some business insights and strategy recommendations are below:

The first graph, “Top X Products by Quantity Sold in 2024”, which is a horizontal bar chart shows the top-selling products by quantity. Wall Clock, Backpack, and Desk Lamp are the highest-selling products. High sales volume does not always mean high revenue. Therefore, focusing on profit margins can be a good idea. Moreover, some high-volume products (like Blue Pens and White Mugs) may need better pricing to maximize profitability.

In the second graph, which is a scatter plot named “Relationship Between Revenue And Quantity Sold For Each Product Type”, analyzing the correlation between revenue and quantity sold of each product. Some of the products with the highest and lowest revenue, and highest and lowest quantity have been annotated. Some products generate high revenue with fewer units sold such as Notebook, while others require higher quantities to achieve similar revenue. Moreover, high-sales, low-revenue products such as Blue Pens and USB Cables might need pricing optimization. Promoting high-revenue items through targeted marketing can be considered.

The third chart, a bubble chart with a title “Product Profitability & Pricing Analysis”, Electronics ($15.54M) and Stationery ($11.72M) are the highest revenue generating categories. Also, furniture has lower revenue compared to its market potential. One of the actions can be introducing premium & bundled pricing to maximize profitability.
In the fourth graph, “Category Wise % YoY Growth”, shows the percentage revenue growth for each product category. While the Electronics category has experienced a massive increase (298%), the categories of Furniture and Stationery have experienced a decline. For the Furniture and Stationery category, different kinds of campaigns can be conducted.
The fifth chart, “Dual Axis Chart Between Revenue and Quantity for Each Category”, is a combined bar and line chart showing quantity sold vs. revenue for each category. While the Electronics category has the highest revenue and highest quantity sold , the lowest revenue and quantity sold belongs to the Apparel category. For the Electronics category, premium marketing can be focused on.

The last chart, “Revenue Based on Product & Category”, is showing revenue per product within each product and category. While creating this horizontal bar chart, Level of Detail (LOD) technique has been applied. LOD (Levels of Detail) technology, initially introduced by Clark in 1976, is dedicated to expediting rendering processes by simplifying the level of detail in a model. More specifically, this technology allocates rendering resources for objects based on their positions and significance within the display environment. It achieves efficient rendering operations by reducing the number of facets and level of detail for less significant objects (Gong et al., 2024). The "Exclude Revenue LOD" field has been created, as explained above previously. This calculated field excludes product names and enables users to analyze data by category.

Dashboard 3: Trend Analysis

The Trend Analysis Dashboard with detailed explanation, some business insights and strategy recommendations are below:

The first graph, “Variation of Revenue Across Quarters in Five Years for Each EU Country”, is showing revenue trends per quarter for EU countries over five years. Different patterns across countries indicate revenue fluctuations based on seasonal demand, economic conditions, or regional factors. Some EU countries show stable revenue trends, while others experience more variability. The reason behind it can be different consumer behavior or market conditions. Focusing on regions with inconsistent revenue trends and strengthening Q4 marketing strategies can be applied.

The second graph, “Total Quantity Sold Over the Months,” displays the total quantity of products sold each month from the beginning of 2020 to the end of 2024, with each year represented in a different color. It clearly shows a dramatic drop in quantity sold every February, with all February bars annotated for clarity. This decline may be due to the conclusion of certain campaigns at the end of January, leading to a decrease in purchases. To overcome this drop, new campaign strategies can be developed specifically for February.

In the third graph, “Yearly Profit Based on Categories”, the area chart illustrates profit contributions from different product categories, which are Electronics, Furniture, Stationery, Furniture, Apparel, and Accessories, over the years. It is shown that while the Electronics category has the highest profit, the Accessories category has the lowest contribution to the overall profit. Considering cross-selling strategies by bundling Electronics with Accessories can increase the overall sales.
The fourth graph, “Cumulative Profit Over the Years”, is again an area chart but this time this chart shows cumulative overall profit to see the differences over the years. Each cumulative profit amount has been annotated for each year.

In the fifth graph, “ Monthly Shipping Cost Trends”, shows how shipping costs fluctuate month-over-month from 2020 to 2024. Moreover, the peak points have been annotated to consider these months while planning the new strategy for the next period. Working with logistics partners to optimize shipping routes might help to decrease the shipping costs.
The last graph, “Monthly Shipping Cost by Shipping Provider”, shows the percentage contribution of different shipping providers such as DHL, FedEx, Royal Mail, and UPS. It is shown that shipping providers contribute similarly to the overall shipping cost. To reduce the total shipping cost, discounts could be applied when a certain threshold amount is exceeded.

INTERACTIVE DASHBOARDS: 
After designing the dashboards, some actions such as filters and highlights have been added to each dashboard. Therefore, all dashboards became user-friendly and interactive.

STORY:

After all three dashboards have been created, the story has been developed by using Tableau’s story feature. The story consists of three sheets, representing each dashboard which are “Countries”, “Products”, and “Trends”.

As a final step, the tableau file is converted from live to extract in order to publish it in the public tableau platform. The link of published tableau file above:

https://public.tableau.com/app/profile/irem.anter/viz/VSTT-Assignment2/SalesAnalysis?publish=yes
