# Supermarket Sales
### Concept Idea
The project focuses on utilizing visualizations to convey a narrative based on supermarket sales data. Various graph types, such as bar graphs, are employed to enhance accessibility and understanding. It aims to analyze the information depicted in the charts to identify areas of strength and improvement for the supermarket. Through this analysis, they seek to generate smart ideas for boosting sales and enhancing customer satisfaction. The project's overarching goal is to transform data into visual stories that offer valuable insights, uncover patterns, and highlight trends to inform decision-making and ultimately improve the supermarket's overall performance.

### Data Source
https://www.kaggle.com/datasets/aungpyaeap/supermarket-sales

### Data Exploration
The dataset comprises 1000 rows and includes columns such as Invoice ID, Branch City, Customer Type, Gender, Product Line, Unit Price, Quantity, Tax 5%, Total, Date, Time, Payment, COGS (Cost of Goods Sold), Gross Margin Percentage, Gross Income, and Rating

The data type in the "Date" column is inconsistent; some dates are in the date data type, while others are not.
![Screenshot 2024-03-31 112832](https://github.com/ochengco-paolo/SupermarketSales/assets/140794262/0ac0a5d4-0b87-4d5b-ac61-4095e6b6f104)

### Data Processing
Since the "Date" column is inconsistent and it needed to be consistent by format dd/mm/yyyy, I firstly execute the **Text to Columns** by delimiter of '/'. After that, I namely the columns by "Day", "Month", and "Year". And as you can see in the screenshot below, I used **Conditional Formatting > Highlight Cell Rules > Greater Than = 12**  in the month column to distinguished all the inconsistent date format in the dataset.
![1](https://github.com/ochengco-paolo/SupermarketSales/assets/140794262/4d814b5b-ebeb-49ce-9189-dd4013c9dbec)

After that, I filtered all the inconsistent Date format and copy all the values that have greater that 12 in the Month and put it in Day column since that is the right position for the data and also with the day to Month. After that, I named the column "NewDay" and "NewMonth" to not be confuse with the process. Also, I added "NewDate" column since this will be the final output for the Date column by using the formula **=DATE(Year, Month, Day)**.
![3](https://github.com/ochengco-paolo/SupermarketSales/assets/140794262/78b16f45-84c9-4c8d-95aa-d36f992c7bf1)
