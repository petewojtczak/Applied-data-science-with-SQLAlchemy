# Applied-Data-Science with SQLAlchemy

## Task 1: Forecasting<br>
The objective of this section is to utilize the transaction_data database in order to develop a system for forecasting demand over a short-term period (21 days), for all product categories.<br><br>

## Task 2: Analysis of sellers and products<br>
In this section, an analytical report is desired on the sellers and products listed on our marketplace. Using the provided data on sellers and products, the report should include details such as the best and worst sellers by state, as well as the best and worst products by category. Additionally, turnover analytics should be investigated to uncover valuable insights.<br><br>

## Task 3: Analysis of product semantics<br>
Our database includes numerical product ratings accompanied by text reviews. Let's implement functionality to classify comments as positive or negative and compile the analytics. I am interested in the correlation between text comments and numerical ratings (1-5), identifying products with the best and worst reviews, and highlighting sellers who receive only negative feedback.

**'order_items'**
Primary Key: order_items_pk
Foreign Key Column(s):
  - order_id
  - product_id
  - seller_id
Columns: ['order_items_pk', 'order_id', 'product_id', 'seller_id', 'price']
Number of Records: 110197

**'order_reviews'**
Primary Key: review_id
Foreign Key Column(s):
  - order_id
Columns: ['review_id', 'order_id', 'review_score', 'review_comment_message']
Number of Records: 39462

**'orders'**
Primary Key: order_id
Foreign Key: None
Columns: ['order_id', 'timestamp', 'customer_contact']
Number of Records: 96478

**'products'**
Primary Key: product_id
Foreign Key: None
Columns: ['product_id', 'product_category_name', 'product_weight_g']
Number of Records: 32216

**'sellers'**
Primary Key: seller_id
Foreign Key: None
Columns: ['seller_id', 'seller_state']
Number of Records: 2970
