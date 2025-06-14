# Financial-Advisory-System-using-Java
# 💰 Smart Financial Tracker and Advisory System

A personal finance management and smart advisory application built using **Java** and **Spring Boot**. This application allows users to manage their income, expenses, financial goals, and spending thresholds — all in one place.

---

## 📌 Features

### ✅ User Management
- Register/Login/Logout
- Update profile and change password
- Secure authentication (JWT or session-based)

### 💸 Financial Transactions
- Track **current income** and **expenses**
- Monitor balance across **multiple modes** (cash, card, bank)
- Record **upcoming** (future-dated) income or expenses

### 🎯 Goal Setting
- Set financial goals (e.g. “Save ₹10,000 for vacation”)
- Track progress toward each goal

### 🧾 Monthly Threshold
- Set a monthly **spending limit**
- Automatic calculation at the **end of each month**
- Uses **Spring Scheduler** and **Cron Jobs** for evaluation

### 🧠 Smart Financial Advisory
- Analyze trends and give **saving/spending suggestions**
- Detect abnormal transactions
- Rule-based logic (extensible to ML in future)

### 🗒️ Notes and Tags
- Create financial **notes** for personal reference
- Add **tags** to transactions for easy filtering and search

---

## 🛠️ Tech Stack

| Layer       | Technology                  |
|-------------|-----------------------------|
| Language    | Java 17+                    |
| Framework   | Spring Boot, Spring MVC     |
| Security    | Spring Security / JWT       |
| ORM         | Hibernate / Spring Data JPA |
| Scheduler   | Spring Scheduler + Cron     |
| Database    | MySQL / PostgreSQL          |
| Frontend    | (Optional) Angular / React  |
| Build Tool  | Maven / Gradle              |
| API Style   | RESTful                     |

---

## 🗃️ Database Schema (Basic Entities)

- **User**
  - id, name, email, password, created_at, updated_at
- **Transaction**
  - id, user_id, amount, type (gain/expense), mode (cash/bank/card), date, note, tags
- **Goal**
  - id, user_id, target_amount, description, deadline, achieved
- **Note**
  - id, user_id, content, tags, created_at
- **Threshold**
  - id, user_id, month, limit_amount, spent_amount
