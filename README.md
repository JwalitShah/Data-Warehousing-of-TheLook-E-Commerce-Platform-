
# TheLook Data Analysis 

### Business Problem

The operational dynamics of TheLook's eCommerce platform are shaped by intense market competition and a relentless pursuit of customer satisfaction. Amidst a fiercely competitive landscape, TheLook confronts the perpetual challenge of meeting and surpassing customer expectations while contending with innovative rivals. Efficiency across operational fronts stands as a linchpin, where seamless order processing, agile inventory management, and optimized logistics directly dictate the company's competitive edge. Embracing data-driven decision-making, TheLook leverages insights extracted from user behavior, sales trends, and demographic analytics to steer strategic initiatives effectively.

At the core of its operational ethos lies the execution of robust marketing strategies and customer engagement tactics, aimed at driving traffic, enhancing conversion rates, and fostering enduring brand loyalty. Concurrently, the optimization of supply chain mechanisms remains pivotal, ensuring prompt order fulfillment while fine-tuning inventory levels and distribution processes. The company's unwavering commitment to cultivating a distinct brand identity and delivering unparalleled customer service underscores its aspiration for market leadership and sustained growth.

In a milieu characterized by rapid technological evolution and evolving consumer preferences, TheLook remains poised for adaptability and innovation. Positioned to seize emerging opportunities and navigate shifting market dynamics, TheLook's operational paradigm is deeply entrenched in agility, data-centricity, and a steadfast commitment to customer-centric excellence. Through a strategic blend of operational prowess, customer-centricity, and a penchant for innovation, TheLook endeavors to not only thrive amidst competition but also redefine benchmarks for success within the dynamic eCommerce landscape.


### Analysis Goals 

1. Total Sales Analysis
Analysis of total sales across geography and clothing category.
This helps the business to understand the places and trends which gets the more sales.


2. Quantity Analysis: 
People with the most quantity of order over the time.
This helps the business to understand loyal customers and help in keeping the rewards.



### Relational Model

1.	Distribution_centers (distribution_center_Id, name, latitude, longitude)

2.	Products (Product_Id, distribution_center_id, cost, category, name, brand, retail_price, department, sku)

distribution_center_id  -> (References distribution_centers(distribution_center_id))

3.	Events (event_id, user_id, sequence_number, session_id, created_at, ip_address, city, state, postal_code, browser, traffic_source, uri, event_type)

user_id  -> (References users (user_id))

4.	Inventory_Items (Inventory_Item_id, product_id, distribution_center_id, created_at, sold_at cost, product_category, product_name, product_brand, product_retail_price, product_department, product_sku)

product_id  -> (References products (product_id))
distribution_center_id  -> (References distribution_centers (distribution_center_id))

5.	order_items (order_item_id, order_id, user_id, product_id, inventory_item_id, status, created_at, shipped_at, delivered_at, returned_at)

order_id  -> (References orders (order_id))
user_id  -> (References users (user_id))
product_id  -> (References products (product_id))
Inventory_Item_id  -> (References Inventory_Items (Inventory_Item_id))

6.	orders (order_id, user_id, status, gender, created_at, returned_at, shipped_at, delivered_at, num_of_item)

user_id  -> (References users (user_id))

7.	users (user_id, first_name, last_name, email, age, gender, state, street_address, postal_code, city, country, latitude, longitude, traffic_source, created_at)


### Data Warehouse Model


<p align="center">
<img src="https://github.com/sanilrod/TheLook-Data-Warehousing/blob/main/Img/logical.drawio%20(2).drawio%20(1).png" border="10"/>
</p>

### Talend Implementations

1. Customer_Dimension

<p align="center">
<img src="https://github.com/sanilrod/TheLook-Data-Warehousing/blob/main/Img/Picture1.png" border="10"/>
</p>

<br>
<br>

<p align="center">
<img src="https://github.com/sanilrod/TheLook-Data-Warehousing/blob/main/Img/Picture2.png" border="10"/>
</p>



2. Events_Dimension

<p align="center">
<img src="https://github.com/sanilrod/TheLook-Data-Warehousing/blob/main/Img/Picture3.png"  border="10"/>
</p>

<br>
<br>

<p align="center">
<img src="https://github.com/sanilrod/TheLook-Data-Warehousing/blob/main/Img/Picture4.png" border="10"/>
</p>


3. Distribution_center_Dimension

<p align="center">
<img src="https://github.com/sanilrod/TheLook-Data-Warehousing/blob/main/Img/Picture5.png"  border="10"/>
</p>

<br>
<br>

<p align="center">
<img src="https://github.com/sanilrod/TheLook-Data-Warehousing/blob/main/Img/Picture6.png"  border="10"/>
</p>


4. Order_Dimension

<p align="center">
<img src="https://github.com/sanilrod/TheLook-Data-Warehousing/blob/main/Img/Picture7.png"  border="10"/>
</p>

<br>
<br>

<p align="center">
<img src="https://github.com/sanilrod/TheLook-Data-Warehousing/blob/main/Img/Picture8.png"  border="10"/>
</p>


5. Product_Dimension

<p align="center">
<img src="https://github.com/sanilrod/TheLook-Data-Warehousing/blob/main/Img/Picture9.png"  border="10"/>
</p>

<br>
<br>

<p align="center">
<img src="https://github.com/sanilrod/TheLook-Data-Warehousing/blob/main/Img/Picture10.png"  border="10"/>
</p>



6. Date_Dimension

<p align="center">
<img src="https://github.com/sanilrod/TheLook-Data-Warehousing/blob/main/Img/Picture11.png" border="10"/>
</p>

<br>
<br>

<p align="center">
<img src="https://github.com/sanilrod/TheLook-Data-Warehousing/blob/main/Img/Picture12.png"  border="10"/>
</p>



6. Fact_Revenue_Dimension

<p align="center">
<img src="https://github.com/sanilrod/TheLook-Data-Warehousing/blob/main/Img/Picture13.png"  border="10"/>
</p>

<br>
<br>

<p align="center">
<img src="https://github.com/sanilrod/TheLook-Data-Warehousing/blob/main/Img/Picture14.png"  border="10"/>
</p>


### Tableau Dashboard

<p align="center">
<img src="https://github.com/sanilrod/TheLook-Data-Warehousing/blob/main/Img/Picture15.png"  border="10"/>
</p>
