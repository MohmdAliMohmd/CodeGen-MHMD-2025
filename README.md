# CodeGen-MHMD-2025

## ✨ Overview

This repository is a part of the CodeGen-MHMD-2025 project, focused on enhancing code generation and structure for .NET-based applications. The goal is to streamline data access and business logic patterns with reusable, efficient components.

---

## 🔧 What's New?

### ✅ Added: `IsFindByColumn` and `IsExistByColumn`

These two new methods were added to **both the Data Layer and Business Layer** to improve flexibility when working with dynamic queries.

---

## 📁 Where Changes Were Made

### 🧱 Data Layer

- **`IsFindByColumn`**  
  Returns an entity (or list) that matches a specific column name and value.

- **`IsExistByColumn`**  
  Returns `true` or `false` based on whether a record exists with a specified column value.

### 🧠 Business Layer

- Mirrors the data layer with the same two methods, acting as an abstraction layer.
- Adds business-level logic if needed before/after checking the database.

---

## 🧪 Example Use Case

```csharp
// Check if a user exists by email
bool exists = userService.IsExistByColumn("Email", "example@email.com");

// Find a user by username
var user = userService.IsFindByColumn("Username", "john_doe");
