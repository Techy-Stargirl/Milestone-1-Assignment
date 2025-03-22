# Milestone 1 Assignment (Insurance Management System)

This repository contains Python code for a basic Insurance Management System, organized into three separate Jupyter Notebooks. The system manages policyholders, products, and payments.

## Structure

The project is divided into the following notebooks:

1.  **Policyholder Class (Policyholder.ipynb):**
    * Defines the `Policyholder` class, which represents an individual policyholder.
    * Includes methods for registering, suspending, and reactivating policyholders.

2.  **Product Class (Product.ipynb):**
    * Defines the `Product` class, which represents insurance products.
    * Provides methods for updating product prices and suspending products.
    * Creates a list of `Product` objects and displays their information.

3.  **Payment Class (Payment.ipynb):**
    * Defines the `Payment` class, which handles payment processing.
    * Includes methods for processing payments, sending reminders, and applying penalties.   

4.  **Policyholder Management (Policyholder Management.ipynb):**
    * Defines the `Policyholder` class, which represents an individual policyholder.
    * Includes methods for registering, suspending, and reactivating policyholders.
    * Demonstrates the creation of `Policyholder` objects and displays their details.
    * Defines the `Payment` class, which handles payment processing.
    * Includes methods for processing payments, sending reminders, and applying penalties.
    * Demonstrates the creation of `Payment` objects and performs payment operations.

## Class Descriptions

### Policyholder Class

```python
class Policyholder:
    def __init__(self, policy_id, name, status="Active"):
        self.policy_id = policy_id
        self.name = name
        self.status = status
        self.payments = []

    def register(self):
        self.status = "Active"
        print(f"Policyholder {self.name} registered successfully.")

    def suspend(self):
        self.status = "Suspended"
        print(f"Policyholder {self.name} suspended.")

    def reactivate(self):
        self.status = "Active"
        print(f"Policyholder {self.name} reactivated.")

- policy_id: Unique identifier for the policyholder.
- name: Name of the policyholder.
- status: Current status of the policyholder (e.g., "Active", "Suspended").
- payments: A list to store payment objects associated with the policyholder.

### Product Class
Python

class Product:
    def __init__(self, product_id, name, price):
        self.product_id = product_id
        self.name = name
        self.price = price

    def update_price(self, new_price):
        self.price = new_price
        print(f"Product {self.name} price updated to {self.price}.")

    def suspend(self):
        print(f"Product {self.name} has been suspended.")

- product_id: Unique identifier for the product.
- name: Name of the insurance product.
- price: Price of the product.

### Payment Class
Python

class Payment:
    def __init__(self, policyholder, product, amount):
        self.policyholder = policyholder
        self.product = product
        self.amount = amount
        self.status = "Paid"
        policyholder.payments.append(self)

    def process_payment(self):
        print(f"Payment of {self.amount} processed for {self.policyholder.name} on product {self.product.name}.")

    def send_reminder(self):
        print(f"Reminder sent to {self.policyholder.name} for payment of {self.amount}.")

    def apply_penalty(self, penalty_amount):
        self.amount += penalty_amount
        print(f"Penalty of {penalty_amount} applied to {self.policyholder.name}. New amount due: {self.amount}.")

- policyholder: The Policyholder object associated with the payment.
- product: The Product object associated with the payment.
- amount: The payment amount.
- status: The payment status (e.g., "Paid").

## Usage
 - Open each .ipynb file in a Jupyter Notebook environment.
- Run the cells in each notebook sequentially to execute the code and observe the output.
- The notebooks demonstrate the creation of objects, method calls, and output display.

## Dependencies
- Python 3.x
- Jupyter Notebook (optional, for viewing and running the .ipynb files)

## Notes
- This is a basic implementation and can be extended to include more features and functionalities.
- The code is designed for educational purposes and demonstrates object-oriented programming concepts.
- Please ensure that you have Jupyter notebook or an environment that can run python notebooks in order to run each file.

Author:
Stellamaris Okeh
stellamarisijeoma0@gmail.com
