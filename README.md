# Applied-Data-Science with SQLAlchemy

## Task 1: Data Analytics<br>
In this section, turnover analytics should be investigated to uncover valuable insights (include short-term aggregated turnover forecast). Additionally, a detailed analytical report is desired on the sellers and products listed on our marketplace.<br>

`Turnover Analytics:` <br>
* Aggregated turnover,
* Turnover in categories,
* Growing Categories,
* Most valuable categories,
* Declining Categories,
* Least valuable categories.<br>

`Sellers Analytics:` <br>
* Top 10 sellers by Revenue,
* Average Order Value by Seller,
* Average daily revenue for each seller,
* Best seller within each category,
* Sellers with the Highest Number of Reviews,
* Top Sellers by Customer Satisfaction Score.<br>

`Products Analytics:` <br>
* Top 10 Products by Revenue,
* Top 10 Products by Total Units Sold,
* Average daily revenue for each product,
* Best product within each category,
* Average Product Weight by Category,
* Average Product Price by Category,
* Average Review Score by Product Category,
* Products with the Highest Number of Reviews,
* Top Products by Customer Satisfaction Score.

## Task 2: Forecasting<br>
The goal is to perform demand forecasting for each product category.<br><br>
Notes:
* Demand is assumed to be synonymous with the value of things,
* Expected forecasting horizon is around 14 days,
* Weekly seasonality is reportedly alleged (according to `Data Card` description).

## Task 3: Analysis of Sentiment<br>
This section implements functionality to classify comments as positive, neutral or negative using RoBERTa model. Fameous transformer architecture.<br><br>
Key findings include `most endorsed products and sellers`.<br>

`Database Updates:` <br>
* Added `sentiment` column into an `order_reviews` table,
*  Added `text_rating` column into an `order_reviews` table.<br><br>

### About Dataset 
The file `transactional_data.db` is an SQLite database that contains five tables relevant to marketplace transactions. Each table captures specific aspects of the transaction process and is designed to support various types of analyses. Here’s an overview of the tables included:

- **`sellers`**: Contains information about sellers, including `seller_id` (pk) and `seller_state`. This table has 2,970 records.
  
- **`products`**: Lists details about products available on the marketplace, including `product_id` (pk), `product_category_name`, and `product_weight_g`. This table includes 32,216 records.

- **`orders`**: Provides details about each order, such as `order_id` (pk), `timestamp`, and `customer_contact`. This table has 96,478 records.

- **`order_items`**: Serves as a container for a set of items associated with each order, with columns such as `order_items_pk` 
(pk), `order_id`(fk), `product_id`(fk), `seller_id`(fk), and `price`. This table contains 110,197 records.

- **`order_reviews`**: Includes reviews associated with each order, with columns like `review_id` (pk), `order_id` (fk), `review_score`, and `review_comment_message`. This table has 39,462 records.

Data source: https://www.kaggle.com/datasets/petewojtczak/raw-transactional-data
