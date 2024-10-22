# Applied-Data-Science with SQLAlchemy

## Task 1: Forecasting<br>
The objective of this section is to utilize the transaction_data database in order to develop a system for forecasting demand over a short-term period (21 days), for all product categories.<br><br>

## Task 2: Analysis of sellers and products<br>
In this section, an analytical report is desired on the sellers and products listed on our marketplace. Using the provided data on sellers and products, the report should include details such as the best and worst sellers by state, as well as the best and worst products by category. Additionally, turnover analytics should be investigated to uncover valuable insights.<br><br>

## Task 3: Analysis of product semantics<br>
Our database includes numerical product ratings accompanied by text reviews. Let's implement functionality to classify comments as positive or negative and compile the analytics. I am interested in the correlation between text comments and numerical ratings (1-5), identifying products with the best and worst reviews, and highlighting sellers who receive only negative feedback.<br><br>

### About Dataset 
The file `transactional_data.db` is an SQLite database that contains five tables relevant to marketplace transactions. Each table captures specific aspects of the transaction process and is designed to support various types of analyses. Here’s an overview of the tables included:

- **`sellers`**: Contains information about sellers, including `seller_id` (pk) and `seller_state`. This table has 2,970 records.
  
- **`products`**: Lists details about products available on the marketplace, including `product_id` (pk), `product_category_name`, and `product_weight_g`. This table includes 32,216 records.

- **`orders`**: Provides details about each order, such as `order_id` (pk), `timestamp`, and `customer_contact`. This table has 96,478 records.

- **`order_items`**: Serves as a container for a set of items associated with each order, with columns such as `order_items_pk` 
(pk), `order_id`(fk), `product_id`(fk), `seller_id`(fk), and `price`. This table contains 110,197 records.

- **`order_reviews`**: Includes reviews associated with each order, with columns like `review_id` (pk), `order_id` (fk), `review_score`, and `review_comment_message`. This table has 39,462 records.

Data source: https://www.kaggle.com/datasets/petewojtczak/raw-transactional-data
