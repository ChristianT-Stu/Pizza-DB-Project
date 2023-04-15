Explination of Iterations for Table Creations: 

(4/14/23) - Iteration 1 
  - Designed my first standard table within QuickDBD. 
    This will take care of the "Orders" that will come into my Pizza Joint, and track relevant information associated to them.
    
    This first iteration table includes the following fields: 
    - row_id int pk
    - order_id varchar(10)
    - created_at datetime
    - item_name varchar(50)
    - item_cat varchar(50)
    - item_size varchar(20)
    - item_price decimal(5,2)
    - quantity int
    - cust_firstname varchar(50)
    - cust_lastname varchar(50)
    - delivery boolean
    - delivery_address1 varchar(200)
    - delivery_address2 varchar(200)
    - delivery_city varchar(50)
    - delivery_zipcode varchar(20)
 
 ![image](https://user-images.githubusercontent.com/69771935/232108605-08abbc19-51e5-4ecd-8594-58208b82be92.png)


(4/15/23) - Iteration 2
  - Repetative info noticed in created table above in Iteration 1.
    Decided to create two more tables to handle excess overflow of info and link these new tables with cust_id, and add_id.
    I have made a Customers table and an Address Table
    
    Customer Table: 
    - cust_id int pk FK >- order.cust_id
    - cust_firstname varchar(50)
    - cust_lastname varchar(50)
    
    Address Table: 
    - add_id int pk FK >- order.add_id
    - delivery_address1 varchar(200)
    - delivery_address2 varchar(200) NULL
    - delivery_city varchar(50)
    - delivery_zipcode varchar(20)
    
 ![image](https://user-images.githubusercontent.com/69771935/232240490-567256e3-2748-4a75-b0f2-273f5c1088a7.png)
 
 
 (4/15/23) - Iteration 3
  - Repetative info noticed in created table above in Iteration 2.
    Decided to create another table to handle item info and link this new table with item_id.
    With this new Item table, if at any point we would want to change any of the item names from the menu, you would only need to change one field in the new table.
    
    Item Table:
    - item_id int pk FK >- order.item_id
    - sku varchar(20)
    - item_name varchar(50)
    - item_cat varchar(50)
    - item_size varchar(20)
    - item_price decimal(5,2)

![image](https://user-images.githubusercontent.com/69771935/232256046-2eb1117a-8dd1-4575-86e1-fcd7d82b916d.png)
