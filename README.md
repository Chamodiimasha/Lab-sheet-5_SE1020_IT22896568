# SE1020 – Object Oriented Programming (Year 1 Semester 2)
## Lab Sheet 05 - Question 03

### Scenario Overview: Online Bookshop System

An Online bookshop sells different things. Currently it has books, magazines and CDs. All these products have some common types of information such as price, title etc.. Also each product may have specific information such as author, number of pages, artists, type etc..

The registered customers can place orders for products. The ordered products are usually delivered together, but sometimes several shipments are needed when the store runs out of products for a while. An order may contain several products.

The products are delivered to personal customers and payments are done at the delivery. The business customers will get their orders directly, and they will be sent an invoice afterwards. Both customer types can make the payment also by using credit card. When registering, a customer is prompted to give contact and personal information needed for authentication, delivery of orders and invoicing.

The bookshop system must be able to add and remove a customer, add new product and view/update existing product, make or remove an order and view existing order, view and generate reports on the products.

---

### Part (a): Potential Nouns Identified

1. Online bookshop / Bookshop / Store / Bookshop system / System
2. Things
3. Books / Book
4. Magazines / Magazine
5. CDs / CD
6. Products / Product
7. Common types of information / Information
8. Price
9. Title
10. Specific information
11. Author
12. Number of pages / Pages
13. Artists / Artist
14. Type
15. Registered customers / Customers / Customer
16. Orders / Order
17. Shipments / Shipment
18. Personal customers / Personal customer
19. Payments / Payment
20. Delivery / Deliveries
21. Business customers / Business customer
22. Invoice
23. Customer types
24. Credit card
25. Contact and personal information
26. Authentication
27. Invoicing
28. Reports / Report

---

### Part (b): Application of the Five Elimination Rules

#### The Five Rules of Class Elimination:
- **Rule 1: Redundant Classes (Synonyms)** – Retain the most descriptive term and eliminate synonyms.
- **Rule 2: Vague Classes** – Reject terms that are ill-defined or too abstract to represent distinct classes.
- **Rule 3: Attributes** – Reject words that describe properties/values of an object rather than an independent entity.
- **Rule 4: Operations / Actions** – Reject words that represent behaviors, actions, or processes.
- **Rule 5: Implementation Constructs / System Boundary** – Reject the system as a whole, database tables, or UI components.

#### Noun Classification & Elimination Table:

| Noun / Noun Phrase | Decision | Reason / Rule Applied |
| :--- | :--- | :--- |
| **Product** | **Accepted** | Generalization / Superclass representing any sellable item. |
| **Book** | **Accepted** | Subclass of `Product` with specific attributes (author, pages). |
| **Magazine** | **Accepted** | Subclass of `Product` with specific attributes (issue, type). |
| **CD** | **Accepted** | Subclass of `Product` with specific attributes (artist, type). |
| **Customer** | **Accepted** | Generalization / Superclass representing buyers. |
| **PersonalCustomer** | **Accepted** | Subclass of `Customer` (pays at delivery or by card). |
| **BusinessCustomer** | **Accepted** | Subclass of `Customer` (receives direct delivery and invoice). |
| **Order** | **Accepted** | Entity representing a customer's purchase request. |
| **Shipment** | **Accepted** | Entity representing dispatch batches when orders are split. |
| **Invoice** | **Accepted** | Entity representing billing statements for business customers. |
| **Payment** | **Accepted** | Entity representing payment transactions (cash / card). |
| **Report** | **Accepted** | Entity representing generated sales and product reports. |
| **Things** | Rejected | **Rule 1 (Redundant)** – Synonym for `Product`. |
| **Registered customers** | Rejected | **Rule 1 (Redundant)** – Synonym for `Customer`. |
| **Customer types** | Rejected | **Rule 1 (Redundant)** – Modeled via class inheritance hierarchy. |
| **Store / Bookshop** | Rejected | **Rule 1 (Redundant)** – Synonym for system boundary. |
| **Common types of information** | Rejected | **Rule 2 (Vague)** – Vague phrase referring to common attributes. |
| **Specific information** | Rejected | **Rule 2 (Vague)** – Vague phrase referring to subclass-specific attributes. |
| **Contact and personal info** | Rejected | **Rule 2 (Vague)** – Vague phrase representing customer attributes. |
| **Information** | Rejected | **Rule 2 (Vague)** – Too general and ill-defined. |
| **Price** | Rejected | **Rule 3 (Attribute)** – Property of `Product`. |
| **Title** | Rejected | **Rule 3 (Attribute)** – Property of `Product`. |
| **Author** | Rejected | **Rule 3 (Attribute)** – Property of `Book`. |
| **Number of pages** | Rejected | **Rule 3 (Attribute)** – Property of `Book`. |
| **Artists** | Rejected | **Rule 3 (Attribute)** – Property of `CD`. |
| **Type** | Rejected | **Rule 3 (Attribute)** – Property of `CD` / `Magazine`. |
| **Credit card** | Rejected | **Rule 3 (Attribute)** – Payment method details of `Payment`. |
| **Authentication** | Rejected | **Rule 4 (Operation)** – Action/method to authenticate users. |
| **Invoicing** | Rejected | **Rule 4 (Operation)** – Action/method to generate invoice. |
| **Delivery** | Rejected | **Rule 4 (Operation)** – Action/method performed by `Shipment`. |
| **Registering** | Rejected | **Rule 4 (Operation)** – Action/method of registering a customer. |
| **Online bookshop** | Rejected | **Rule 5 (System Boundary)** – Represents the system as a whole. |
| **Bookshop system / System** | Rejected | **Rule 5 (System Boundary)** – Overall software application boundary. |

---

### Final Selected Set of Potential Classes:
1. **`Product`** (Superclass)
2. **`Book`** (Subclass of Product)
3. **`Magazine`** (Subclass of Product)
4. **`CD`** (Subclass of Product)
5. **`Customer`** (Superclass)
6. **`PersonalCustomer`** (Subclass of Customer)
7. **`BusinessCustomer`** (Subclass of Customer)
8. **`Order`**
9. **`Shipment`**
10. **`Invoice`**
11. **`Payment`**
12. **`Report`**
