# SE1020 – Object Oriented Programming (2025)
## Lab Sheet 05 - Question 03 Answers

---

### Scenario Overview: Online Bookshop System

---

### Part (a): Identify all the Nouns which can be potential classes

From the scenario description, the identified nouns (and noun phrases) are:

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

### Part (b): Identify the set of potential classes, showing clearly how the nouns were rejected using the five rules

#### The Five Rules for Class Elimination:
- **Rule 1: Redundant Classes (Synonyms)** – Words referring to the same concept; one is retained and others discarded.
- **Rule 2: Vague Classes** – Words with ill-defined boundaries or that are too ambiguous/general.
- **Rule 3: Attributes** – Words representing properties or values belonging to another entity rather than an independent object.
- **Rule 4: Operations / Actions** – Words representing methods, processes, or actions.
- **Rule 5: Implementation Constructs / System Boundary** – Words representing the system itself or technical implementation details.

#### Noun Classification & Elimination Table:

| Noun / Noun Phrase | Decision | Reason / Rule Applied |
| :--- | :--- | :--- |
| **Product** | **Accepted** | Generalization / Superclass representing any sellable item. |
| **Book** | **Accepted** | Specific subclass of `Product` with unique attributes (author, pages). |
| **Magazine** | **Accepted** | Specific subclass of `Product` with specific attributes (issue, type). |
| **CD** | **Accepted** | Specific subclass of `Product` with specific attributes (artist, type). |
| **Customer** | **Accepted** | Generalization / Superclass representing buyers in the system. |
| **PersonalCustomer** | **Accepted** | Subclass of `Customer` (pays on delivery or by credit card). |
| **BusinessCustomer** | **Accepted** | Subclass of `Customer` (invoiced after direct delivery). |
| **Order** | **Accepted** | Entity representing a customer's purchase request of multiple products. |
| **Shipment** | **Accepted** | Entity representing delivery batches when an order is split. |
| **Invoice** | **Accepted** | Entity representing the billing document sent to business customers. |
| **Payment** | **Accepted** | Entity representing financial transactions (cash on delivery / credit card). |
| **Report** | **Accepted** | Entity representing generated product and sales reports. |
| **Things** | Rejected | **Rule 1 (Redundant)** – Synonym for `Product`. |
| **Registered customers** | Rejected | **Rule 1 (Redundant)** – Synonym for `Customer`. |
| **Customer types** | Rejected | **Rule 1 (Redundant)** – Modeled via inheritance hierarchy (`PersonalCustomer`, `BusinessCustomer`). |
| **Store / Bookshop** | Rejected | **Rule 1 (Redundant)** – Synonym for `Online bookshop` / System boundary. |
| **Common types of information** | Rejected | **Rule 2 (Vague)** – Vague phrase referring to common attributes of `Product`. |
| **Specific information** | Rejected | **Rule 2 (Vague)** – Vague phrase referring to subclass-specific attributes. |
| **Contact and personal info** | Rejected | **Rule 2 (Vague)** – Vague phrase representing attributes of `Customer`. |
| **Information** | Rejected | **Rule 2 (Vague)** – Too general and ill-defined. |
| **Price** | Rejected | **Rule 3 (Attribute)** – Property of `Product`. |
| **Title** | Rejected | **Rule 3 (Attribute)** – Property of `Product`. |
| **Author** | Rejected | **Rule 3 (Attribute)** – Property of `Book`. |
| **Number of pages** | Rejected | **Rule 3 (Attribute)** – Property of `Book`. |
| **Artists** | Rejected | **Rule 3 (Attribute)** – Property of `CD`. |
| **Type** | Rejected | **Rule 3 (Attribute)** – Property of `CD` / `Magazine`. |
| **Credit card** | Rejected | **Rule 3 (Attribute)** – Payment method details/attribute of `Payment`. |
| **Authentication** | Rejected | **Rule 4 (Operation)** – Action/method to verify customer credentials. |
| **Invoicing** | Rejected | **Rule 4 (Operation)** – Action/process performed to issue an invoice. |
| **Delivery** | Rejected | **Rule 4 (Operation)** – Action performed by `Shipment` / store. |
| **Registering** | Rejected | **Rule 4 (Operation)** – Action/method of adding a customer. |
| **Online bookshop** | Rejected | **Rule 5 (System Boundary)** – Represents the entire system itself. |
| **Bookshop system / System** | Rejected | **Rule 5 (System Boundary)** – Represents the whole software boundary. |

---

#### Final Selected Set of Potential Classes:
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
