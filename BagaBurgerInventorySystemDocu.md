# Baga Burger Inventory System

## A. Introduction

## B. Project Features and Characteristics

## C. Project Scope

## D. Work Breakdown Structure

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
