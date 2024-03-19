
# Amazon E-Commerce Report

### Report Link : https://app.powerbi.com/reportEmbed?reportId=093d1f8b-3f7b-4c75-bdec-0cf92c8f959b&autoAuth=true&ctid=6b2b9958-0b17-48e1-b985-40c7199284ef


### Project Overview:
Welcome to my Power BI Amazon E-commerce Report project! This report provides comprehensive insights into various aspects of Amazon sales, products, and customer interactions. Using Power BI, I have created three main pages: Dashboard, Products, and Product View. Additionally, I have implemented several DAX functions to make the report dynamic and insightful.

### Project Objectives:
- Overall Sales: Calculate and visualize the total sales value for the selected period.
- Return Units: Track and display the number of units returned by customers.
Reviews: Display the total number of reviews received for Amazon fashion products.
- Seller Count: Calculate the number of unique sellers based on delivered orders.
- Sale Option: Provide a dynamic table to switch between sales and units view.
- Search Functionality: Enable search functionality to search for specific products within the dataset.


### Dashboard Pages:
- Dashboard:

    Overview of key metrics like total sales, return units, reviews, and seller count.
    Visualizations for sales trends, return analysis, and seller distribution.
    Dynamic selection for sales or units view using the Sale Option table.
    Search box enabled to search for products in the dataset.
- Products:

    Detailed insights into products sold, profit margins, and sales performance.
    Comparison with the previous year's sales and profit figures.
    Total cost analysis and profitability metrics.
    Search box enabled for product search within the dataset.
- Product View:

    On-click functionality to view individual product performance.
    Sales, profit, and return analysis for each product.
    Interactive filters for date, city, product, and channel for personalized analysis.
    Search functionality to find specific products quickly.
### DAX Functions Used:
Here are some of the DAX functions I've utilized in this report:

- Overall Sales: CALCULATE(SUM(Amazon[Total_Amount]),ALL())
- Return Units: var val= CALCULATE(COUNT(Amazon[Order ID]),CONTAINSSTRING(Amazon[Status],"Return")) return IF(val=BLANK(),0,val)
- Reviews: var val = SUM('amazon-fashion - YT'[no_of_reviews]) RETURN IF(val = BLANK(),"0",val)
- Seller Count: CALCULATE([Sale_Units],ALL('amazon-fashion'[Category])) var val = CALCULATE(COUNT('amazon-fashion'[seller_id]),CONTAINSSTRING(Amazon[Status],"Delivered")) Return val
- Sale Option: DataTable("Type", STRING,"Name”, STRING ,{{"1","Sales"},{"2","Units"}})

### How to Use:
Clone this repository to your local machine.
Open the Power BI report file (.pbix) using Power BI Desktop.
Refresh data sources if necessary and ensure all dependencies are resolved.
Interact with the report using slicers, filters, and dynamic selections to explore data insights.
Customize visuals or add new features as per your requirements.

### Acknowledgments:
I would like to acknowledge the support and resources provided by Amazon's data API and Power BI community forums, which helped in creating this insightful e-commerce report. I will keep updating the pages with new functionalities and will publish accordingly.

Feel free to reach out for any questions or feedback related to this project. Happy analyzing!

## Snapshots of Report Published to Power BI Services

![image](https://github.com/RhugvedSatardekar/Amazon-E-commerce-Report/assets/163725285/6b2534c9-364a-45bc-a506-d6e914ecfba9)

![image](https://github.com/RhugvedSatardekar/Amazon-E-commerce-Report/assets/163725285/839a1f40-bc8b-4279-89d3-724a3208b00d)

![image](https://github.com/RhugvedSatardekar/Amazon-E-commerce-Report/assets/163725285/1e4d6baa-1bae-45d7-a1fa-a9144e738463)
