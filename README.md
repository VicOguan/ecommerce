# 🛒 E-Commerce Platform

A collaborative e-commerce application built with a microservice/modular architecture. This repository serves as the central codebase for backend and frontend development, database migrations, and API documentation.

---

## 🛠️ Tech Stack & Tooling

| Category | Tools / Technologies |
| :--- | :--- |
| **IDEs / Editors** | IntelliJ IDEA, Visual Studio Code |
| **Database** | MySQL (Managed via MySQL Workbench) |
| **API Testing** | Postman |
| **Version Control** | Git & GitHub |

---
# 👥 Task Allocation & Collaboration Plan

| Role | Module Focus | Primary Files / Responsibilities |
| :--- | :--- | :--- |
| **Person A** | Core Models & Domain Logic | • **`model/`**: `Product.java`, `Customer.java`, `OrderItem.java`, `Order.java`<br>• **`service/`**: `InventoryService.java`, `OrderService.java` |
| **Person B** | Payment Integrations & Main Flow | • **`payment/`**: `PaymentMethod.java`, `CreditCardPayment.java`, `EWalletPayment.java`<br>• **`Main.java`**: Application setup, scenario testing, end-to-end flow |

---

# 📋 Coding Standards & Variable Naming Cheat Sheet

To keep the codebase clean and avoid integration conflicts, both developers must adhere to the following conventions:

## Naming Conventions Summary

* **Packages:** Lowercase singular (`model`, `service`, `payment`)
* **Classes & Interfaces:** `PascalCase` (`InventoryService`, `PaymentMethod`)
* **Methods:** `camelCase` (`processPayment()`, `calculateTotal()`)
* **Variables / Fields:** `camelCase` (`productName`, `stockQuantity`)
* **Constants:** `UPPER_SNAKE_CASE` (`DEFAULT_TAX_RATE`)

## Standardized Model & Field Names

* **`Product.java`**: `productId`, `name`, `price`, `stockQuantity`
* **`Customer.java`**: `customerId`, `name`, `email`
* **`OrderItem.java`**: `product`, `quantity`
* **`Order.java`**: `orderId`, `customer`, `items` (List), `totalAmount`, `status`

## Standardized Method Signatures

* **`PaymentMethod.java`**: `boolean processPayment(double amount)`, `String getTransactionStatus()`
* **`InventoryService.java`**: `checkStock(String productId, int quantity)`, `reduceStock(String productId, int quantity)`
* **`OrderService.java`**: `createOrder(Customer customer, List<OrderItem> items)`, `processOrderPayment(Order order, PaymentMethod method)`

## 📂 Repository Structure

```text
├── frontend/              # Frontend Web Application (VS Code)
│   ├── .vscode/           # Workspace settings & extension recommendations
│   ├── public/            # Static assets
│   ├── src/               # React / Vue / Angular component source files
│   └── package.json       # Frontend dependencies and scripts
│
├── backend/               # Java Backend Application (IntelliJ IDEA)
│   ├── .idea/             # IntelliJ workspace settings (Git ignored)
│   ├── src/               # Java source code
│   │   ├── model/         # Product, Customer, Order, OrderItem
│   │   ├── service/       # InventoryService, OrderService
│   │   ├── payment/       # PaymentMethod, CreditCardPayment, EWalletPayment
│   │   └── Main.java      # Main execution entry point
│   └── pom.xml / build.gradle
│
├── db/                    # Database Scripts & Schema Management
│   └── migrations/        # Versioned MySQL SQL migration scripts
│       ├── V1__init_schema.sql
│       └── V2__add_products_table.sql
|
├── .editorconfig          # Shared code style rules across VS Code and IntelliJ
├── .gitignore             # Ignored files (build outputs, secrets, local settings)
└── README.md

