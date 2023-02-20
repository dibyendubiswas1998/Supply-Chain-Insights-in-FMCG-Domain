## Data Descriptions:

This file contains all the meta information regarding the columns described in the CSV files. we have provided 3 CSV files:
* **dim_customers.csv**
* **dim_products.csv**
* **dim_date**
* **dim_targets_orders**
* **fact_order_lines.csv**
* **fact_orders_aggregate.csv**

---------------------------------------------------------------------------------------------

### dim_customers:

This table contains all the information about customers

* **customer_id:** Unique ID is given to each customer
* **customer_name:** Name of the customer
* **city:** It is the city where the customer is present

---------------------------------------------------------------------------------------------------

### dim_products:
This table contains all the information about the products

* **product_name:** It is the name of the product
* **product_id:** Unique ID is given to each of the products
* **category:** It is the class to which the product belongs

---------------------------------------------------------------------------------------------------

### dim_date:
This table contains the dates at daily, monthly level and week numbers of the year

* **date:** date at the daily level
* **mmm_yy:** date at the monthly level
* **week_no:**** week number of the year as per the date column

---------------------------------------------------------------------------------------------------

### dim_targets_orders:
This table contains all target data at the customer level

* **customer_id:** Unique ID that is given to each of the customers
* **ontime_target %:** Target assigned for Ontime % for a given customer
* **infull_target %:** Target assigned for infull % for a given customer
* **otif_target %:**   Target assigned for otif % for a given customer

---------------------------------------------------------------------------------------------------

### fact_order_lines:
This table contains all information about orders and each item inside the orders.

* **order_id:** Unique ID for each order the customer placed
* **order_placement_date:** It is the date when the customer placed the order
* **customer_id:** Unique ID that is given to each of the customers
* **product_id:** Unique ID that is given to each of the products
* **order_qty:** It is the number of products requested by the customer to be delivered
* **agreed_delivery_date:** It is the date agreed between the customer and Atliq Mart to deliver the products
* **actual_delivery_date:** It is the actual date Atliq Mart delivered the product to the customer
* **delivered_qty:** It is the number of products that are actually delivered to the customer


---------------------------------------------------------------------------------------------------

### fact_orders_aggregate:
This table contains information about OnTime, InFull and OnTime Infull information aggregated at the order level per customer

* **order_id:** Unique ID for each order the customer placed
* **customer_id:** Unique ID that is given to each of the customers
* **order_placement_date:** It is the date when the customer placed the order
* **on_time:** '1' denotes the order is delviered on time. '0' denotes the order is not delivered on time.
* **in_full:** '1' denotes the order is delviered in full quantity. '0' denotes the order is not delivered in full quantity.
* **otif:**    '1' denotes the order is delviered both on time and in full quantity. '0' denotes the order is either not delivered on time or not in full quantity.

