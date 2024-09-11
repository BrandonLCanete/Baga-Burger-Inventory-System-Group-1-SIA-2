# Baga Burger Inventory System

## A. Introduction
Our group is centered around developing an inventory management system for Baga Burger, a popular burger store at Bagong Silang, Caloocan. Baga burger is a restaurant that specializes in serving burgers, typically with a meat patty, toppings, and condiments, often accompanied by sides like fries and drinks. The system will focus on the store's operations by efficiently tracking stock levels, managing ingredients, and minimizing waste. By automating the inventory process, Baga Burger can ensure timely restocking, avoid shortages, and improve overall productivity, helping the business scale more effectively.

An inventory system is a software or process used to track, manage, and control the flow of goods, materials, or products in a business. It monitors stock levels, orders, sales, and deliveries to ensure that the right amount of inventory is available at all times. By efficiently managing stock, an inventory system helps businesses avoid overstocking, minimize shortages, and optimize reordering processes, leading to cost savings and smoother operations. Having a Real-Time Stock Tracking it monitors inventory levels to ensure products are always available when needed. SAN (Stock Alerts and Notifications) which sends alerts when stock is low to prevent shortages. Order Management that tracks incoming stock and updates inventory when new items are received. Reporting and Analytics which Provides simple reports on stock levels, usage, and trends. Inventory Categorization the one that organizes products into categories for easy tracking.

## B. Project Features and Characteristics

The proposed project Baga Burger Inventory System consists of the following features:

1.	Real-Time Stock Tracking - Tracks inventory to keep products available.
2.	Stock Alerts and Notifications - Alerts when stock is low to avoid shortages.
3.	Order Management - Updates inventory when new stock arrives.
4.	Inventory Categorization - Sorts products for easy tracking.
5.	Reporting and Analytics - Generates basic stock and usage reports.


## C. Project Scope
The Baga Burger Inventory System is an advanced inventory management solution tailored for the operations of a burger restaurant. Given the dynamic nature of foodservice operations, effective inventory management is critical for maintaining smooth operations, ensuring the availability of essential ingredients, and minimizing waste. This system is designed to automate the tracking of various restaurant supplies, such as burger patties, buns, condiments, vegetables, beverages, packaging materials, and other critical ingredients required for daily operations.

In a fast-paced environment like a burger restaurant, manually managing inventory can lead to a variety of issues, including over-ordering, under-stocking, spoilage, and operational delays. The Baga Burger Inventory System aims to reduce the reliance on manual processes and minimize human errors, ensuring that restaurant staff can focus more on providing quality service rather than worrying about inventory shortages or discrepancies.

By automating key inventory processes, the system will allow restaurant managers to gain real-time insights into stock levels, ingredient consumption trends, and potential supply chain gaps. With features such as automated alerts for low stock levels and items nearing expiration, the system will help prevent stockouts and ensure that fresh ingredients are always available. Additionally, the system will enable users to track ingredient usage based on sales patterns, which will help in making data-driven decisions about restocking, purchasing, and forecasting future demand.

The Baga Burger Inventory System is also equipped to generate detailed reports that will help restaurant management analyze inventory performance over time, reduce costs associated with waste or excess stock, and improve the overall efficiency of operations. Moreover, the system will streamline the procurement process by allowing for easy creation of purchase orders directly from within the platform when inventory reaches predefined thresholds. This will save time and enhance the accuracy of replenishing stock.

Ultimately, the Baga Burger Inventory System will provide a comprehensive solution to the challenges of inventory management, resulting in improved operational efficiency, reduced waste, cost savings, and a more reliable supply of ingredients for the restaurant.

## D. Work Breakdown Structure
![image](https://github.com/BrandonLCanete/Baga-Burger-Inventory-System-Group-1-SIA-2/blob/main/baga%20burger.png?raw=true)

## E. Functional Requirements

1. User Requirements

2. Use Case

## F. Database Architecture

### Data Dictionary

#### Table 1: Account Informations

Users: 

| COLUMN NAME | DATA TYPE                        | LENGTH | SAMPLE | DESCRIPTION        |
|------------|-----------------------------------|--------|--------|---------------|
| user_id    | int(pk)                           | 255    | 1      | Number that will encrement if a user make an account |  
| user_name  | varchar                           | 100    | Juan Dela Cruz| A name for users |
| user_email | varchar                           | 150    | juandelacruz@gmail.com | User email to login |
| user_password| varchar                         | 255    | $2y$10$WhIPyfbmpj8lQwG38r26Uu0S7a/BUceLz7BLx/aK0aS | User password to login |
| user_number| int                               | 12     | 639993467999| User phone number |
| user_picture| varchar                          | 150    | profile.jpg | User profile picture |
| user_status| boolean                           | 10     | online      | User online or offline status |

Admin:

| COLUMN NAME | DATA TYPE                        | LENGTH | SAMPLE | DESCRIPTION        |
|------------|-----------------------------------|--------|--------|---------------|
| admin_id   | int(pk)                           | 255    | 1      | Number that will encrement if a admin make an account | 
| admin_name | varchar                           | 100    | Jhonny Papa | A name for admin |
| admin_email| varchar                           | 150    | jhonnypapa@gmail.com | admin email to login |
| admin_password| varchar                        | 255    | $2y$10$WhIPyfbmpj8lQwG38r26Uu0S7a/BUceLz7BLx/aK0bC | admin password to login |
| admin_picture| varchar                         | 150    | profile_admin.jpg | admin profile picture |
| admiin_status| boolean                         | 10     | true      | admin online or offline status |

#### Table 2: Product Information

| COLUMN NAME | DATA TYPE                        | LENGTH | SAMPLE | DESCRIPTION        |
|------------|-----------------------------------|--------|--------|---------------|
| product_id | int(pk)                           | 255    | 1      | Number that will encrement if a product is uploaded in inventory system | 
| product_name | varchar                         | 100    | Patty  | A name for product in inventory |
| product_stock| int                             | 255    | 22     | Product stock in inventory |
| product_description| varchar                   | 150    | This patty has only 22 stock out of 25 | A Description for the stock of the products or what is that product |
| product_picture| varchar                       | 150    | patty.jpg | The picture of the product |
| product_created| datetime                      | 150    | 2024-5-9  | The product uploaded in the inventory system |
| product_confirmation| boolean                  | 10     | True      | A Product need a confirmation from admin if its okay or not | 
| product_deteriorate| datetime                  | 150    | 2024-5-20 | The product date when it will deteriorate |

#### Table 3: Messages

| COLUMN NAME | DATA TYPE                        | LENGTH | SAMPLE | DESCRIPTION        |
|------------|-----------------------------------|--------|--------|---------------|
| message_id | int(pk)                           | 255    | 1      | Number that will encrement if a someone message to other | 
| account_id | int                               | 255    | 2      | The account id of the messenger |
| account_name | varchar                         | 150    | Jason  | The account name of the messenger |
| account_role | enum                            | 150    | users  | The role of the messenger |
| message      | mediumtext                      | 20000  | This product need to restock | The message of the messenger |
| message_created| datetime                      | 150    | 2024-5-9  | The date when the message created |
| account_picture| varchar                       | 150    | profile.jpg | The profile picture of the account |

#### Table 4: Product Notifications

| COLUMN NAME | DATA TYPE                        | LENGTH | SAMPLE | DESCRIPTION        |
|------------|-----------------------------------|--------|--------|---------------|
| notification_id | int(pk)                      | 255    | 1      | Number that will encrement if a notification for product is made  | 
| product_id | int                               | 255    | 2      | The product id |
| product_name | varchar                         | 150    | Buns   | The product name that receive changes |
| notification_message | varchar                 | 1500    | The Buns is now restock  | The notification message of the product that receive changes |

#### Table 5: Password Resets 

| COLUMN NAME | DATA TYPE                        | LENGTH | SAMPLE | DESCRIPTION        |
|------------|-----------------------------------|--------|--------|---------------|
| reset_id | int(pk)                             | 255    | 1      | Number that will encrement if someone reset their password| 
| account_id | int                               | 255    | 2      | The account id |
| account_role | varchar                         | 150    | admin  | The role of the account |
| reset_token  | varchar                         | 1000   |  4881be644b83518cb6d9978a784d81de | The reset token for the password reset |



### ERD






## Non Functional Requirements

### Product Requirement (PLEASE SKIP THIS)

### Organizational Requirement (PLEASE SKIP THIS)

### External Requirements (PLEASE SKIP THIS)

## System Testing and Evaluation (PLEASE SKIP THIS)

### Functional Testing Procedure (PLEASE SKIP THIS)

### Functional Testing Summary

### Evaluation Procedure

### Recommendation

### Wireframe (PLEASE SKIP THIS)

### High Fidelity (PLEASE SKIP THIS)

### System Screenshot (PLEASE SKIP THIS)
