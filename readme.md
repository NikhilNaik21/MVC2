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

ProductBeanInfo:
 
getEntries():
This Java function retrieves all entries from a MySQL database table named "products" and returnsthem as a list of product objects.
@return A List of product objects is being returned.


Project.jsp:

This is a JSP (JavaServer Pages) file that displays a list of products using data from a Java bean called `Sales.ProductInfoBean`. The HTML code contains a table with three columns: Product No, Unit Price, and Current Stock. The `c:forEach` tag is used to iterate over the list of products in the `productInfo` bean and display each product's information in a row of the table. The `${...}` syntax is used to access the properties of each product object. The `<%@ page %>` directive is used to set the language and character encoding for the JSP page, while the `<%@ taglib %>` directive is used to import the JSTL (JavaServer Pages Standard Tag Library) core tag library. The `<jsp:useBean>` tag is used to instantiate a new instance of the `Sales.ProductInfoBean` class and assign it to the `productInfo` variable.


Package pages
Class Day1
java.lang.Object
javax.servlet.GenericServlet
javax.servlet.http.HttpServlet
pages.Day1
All Implemented Interfaces:
Serializable, javax.servlet.Servlet, javax.servlet.ServletConfig

