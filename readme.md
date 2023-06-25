JDBC project to display data in tabular manner fetched from database(MySQL) using MVC2 architecture.

database scripts:

create database cdac;

use cdac;

CREATE TABLE products
(
    product_no integer primary key,
    product_price integer NOT NULL,
    current_stock integer NOT NULL
    
);

INSERT INTO products(
	product_no, product_price, current_stock)
	VALUES (105, 2253, 8);
 
select * from products;

![image](https://github.com/NikhilNaik21/MVC2/assets/111115551/4fc7cbd7-f6b7-415b-b56b-970f56106c62)


Code Explanation:


datamembers (product-POJO class):

private int productNo;
	private int price;
	private int stock;

These are instance variables of the `product` class representing the product number, price, and
 stock of a product. They are declared as private, which means they can only be accessed within the
`product` class and not from outside. They can be accessed and modified using public getter and
setter methods.

