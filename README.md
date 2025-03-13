# Tableau-Projects

Before performing the country, product and trend analysis the data should be understood well and data cleaning processes have been performed. Online Sales dataset, which is obtained from Kaggle with a title “Online Sales Dataset”, includes seventeen attributes, which are as follows:
● InvoiceNo: A unique identifier for each transaction.
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

Additionally, Key Performance Indicators (KPIs) has been defined. calculated fields, sets, parameters, dynamic measures, and filters have been created using relevant formulas by using Tableau. The additional attributes are described in detail below:
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

Moreover, the detail explanation of the parameters and sets as follows:
● Top X Products by Quantity Sold: The top X products are determined based on quantity sold, with the selectable range between 1 and 11.
● Select Measure Name: Enables the user to choose between quantity or revenue as the measure to analyze.
● EU Set: A predefined selection of European countries.
● Description Set 2: Allows the user to select a number between 1 and 11 to display the top X
products in descending order based on quantity sold.

Dashbord 1: Country Analysis

The Country Analysis Dashboard with detailed explanation, some business insights and strategy recommendations are below.

The first visual, “Product Sold by Country (Not Returned)”, shows the relevant sales countries with different colors on the world map. By considering the amount of product sold, returned items are excluded to see the actual amount sold.

In the second chart, “Retailer Country Wise Financial Performance”, colored circles represent average profit amounts of each EU Country. In order to analyze only EU Countries, the EU set has been created before and then added to the filter area by creating this chart. It is shown that there is a slight difference between EU countries in terms of average profit. Therefore, strategic action to increase the profit can be applied equally to all countries.

In the third chart, “Return Rate Across Countries”, return rates have been calculated and it revealed that the highest return rate belongs to the Netherlands. The shipping cost can be increased a little to decrease the number of return items. Moreover, the survey can be hold with the customer who returned the items to understand the main reasons behind it.

The fourth chart, “Order Priority Across Countries”, shows both quantity sold and revenue of each country by selecting these measures from the Measure Dynamic. The colors shows whether the purchase happened in store or online. The United Kingdom and France show a slightly higher share of online orders, while Australia and Italy have more in-store orders.

In the last chart, “Margin Analysis by Product Category in Countries”, x-axis has been divided by EU Countries, and each country divided into products. Y-axis represents the computed profit margin at an aggregate level and the values range from 0 to slightly above 1, showing relative profitability. While blue bars indicate products with an overall margin at or below the threshold, orange bars highlight products with a higher-than-average margin within each country. This classification helps determine which product categories are performing better in terms of profit. Most product categories maintain a similar profit margin across countries. Some products, such as USB Cables and White Mugs, appear in orange, indicating higher margins in those categories for certain countries. The chart enables to identify profitable products per country and supports decision making in sales strategies, price adjustments, and inventory prioritization.

Dashboard 2: Product Analysis

The Product Analysis Dashboard with detailed explanation, some business insights and strategy recommendations are below:



