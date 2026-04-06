# ER-Diagram--Insta-Thrift-Creator-Store-DB-
This Entity Relationship diagram represents the database design for a small Instagram-based store selling thrifted and handmade products. It models the key parts of the business and their relationships to help manage products, customers, orders, payments, shipping, and inventory effectively.

Main Entities and Relationships:
Users (Customers): Stores customer details such as username, email, phone, and address.
Products: Represents thrift and handmade items with attributes like price, category, type, condition, and creation date.
Inventory: Tracks stock availability and flags unique thrift items.
Orders: Each order is linked to one customer and contains multiple products through the Order Items junction table.
Order Items: Connects orders and products, storing quantity and purchase price details.
Payments: Records payment information, including method, status, and transaction details for each order.
Shipping: Tracks shipping address, status, tracking number, and delivery dates related to each order.
Product Variants: Handles product-specific options such as size and color for more detailed inventory management.

Key Relationships:
One customer can place many orders.
One order can include multiple products, and products can be part of many orders (many-to-many resolved by order_items).
Each product has a corresponding inventory record.
Each order is associated with exactly one payment and one shipping record.
Products may have multiple variants, such as different sizes or colors.
