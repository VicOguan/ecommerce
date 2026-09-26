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
│   ├── src/               # Java source code (Spring Boot / Jakarta EE)
│   │   ├── main/
│   │   └── test/
│   └── pom.xml / build.gradle  # Java build & dependency configuration
│
├── db/                    # Database Scripts & Schema Management
│   └── migrations/        # Versioned MySQL SQL migration scripts
│       ├── V1__init_schema.sql
│       └── V2__add_products_table.sql
|
├── .editorconfig          # Shared code style rules across VS Code and IntelliJ
├── .gitignore             # Ignored files (build outputs, secrets, local settings)
└── README.md
