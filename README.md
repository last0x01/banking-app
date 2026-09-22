# Bank Management System

![C#](https://img.shields.io/badge/language-C%23-178600?logo=csharp&logoColor=white)
![.NET](https://img.shields.io/badge/.NET%20Framework-4.8-blue)
![WinForms](https://img.shields.io/badge/UI-WinForms-512BD4)
![SQL Server](https://img.shields.io/badge/Database-SQL%20Server%202022-CC2927?logo=microsoftsqlserver&logoColor=white)
![ADO.NET](https://img.shields.io/badge/ADO.NET-Data%20Access-orange)
![Architecture](https://img.shields.io/badge/Architecture-3--Tier-blue)

A complete desktop banking application built with **C# WinForms** and **ADO.NET**, backed by **SQL Server 2022**. The system is organized in a **3-tier architecture** (Presentation, Business Logic, Data Access) for clean separation of concerns, maintainability, and scalability.

---

## Architecture

```
┌───────────────────┐      ┌──────────────────┐      ┌─────────────────────┐
│  Presentation     │ ───▶ │  Business Layer  │ ───▶ │  Data Access Layer  │
│  "Bank Management │      │  Client / User / │      │  ADO.NET + SQL      │
│   System" (UI)    │      │  TransferLogs    │      │  Server 2022        │
└───────────────────┘      └──────────────────┘      └─────────────────────┘
```

- **Presentation Layer** — `Bank Management System` (WinForms UI)
- **Business Logic Layer** — `BankBusinessLayer` (`Client`, `User`, `Person`, `TransferLogs`, `Global`)
- **Data Access Layer** — `BankDataAccessLayer` (`ClientsData`, `UsersData`, `LoginRegistersData`, `TransferLogsData`, `clsDataAccessSettings`)

---

## Features

### Dashboard
- Total number of customers
- Total number of system users
- Total balance held by the bank
- Number of recorded login attempts
- Number of account-to-account transfers

### Customers Module
- Add, update, delete, search, and list all customers

### Users Module
- Full CRUD management of system users

### Transactions Module
- Deposit into a customer account
- Withdraw from a customer account
- Transfer funds between accounts
- View total bank balance
- Detailed transaction history logs

### Authentication & Authorization
- Secure login screen with a full login-attempts log
- Role- and permission-based access to restrict sensitive operations
- Brute-force protection: the application **automatically closes after 3 failed login attempts**

---

## Requirements

- Visual Studio 2022 (Community or higher)
- .NET Framework 4.8
- SQL Server 2022 Developer Edition (or compatible)
- ADO.NET

---

## Getting Started

1. Clone the repository:

   ```bash
   git clone https://github.com/last0x01/banking-app.git
   ```

2. Open `Bank Management System.sln` in Visual Studio.

3. Create the `Bank` database on your SQL Server instance and configure the connection string in `clsDataAccessSettings.cs`.

4. Restore your schema/data (create tables and seed the sample data).

5. Build and run the project.

> **Note:** The login screen rejects access after **3 failed attempts**, so use the correct system user credentials when testing.

---

## Screenshots

### Login Screen
<img width="390" alt="Login" src="https://github.com/user-attachments/assets/1f9594b6-f446-4ab4-ba62-f7f511d84724" />

### Home Screen
<img width="497" alt="Home" src="https://github.com/user-attachments/assets/23108c44-baf1-4954-a282-86d7b6493ea5" />

### Clients Screen
<img width="497" alt="Clients" src="https://github.com/user-attachments/assets/c0110aa4-f13f-4b34-b01e-6f285488dfeb" />

### Users Screen
<img width="497" alt="Users" src="https://github.com/user-attachments/assets/5bf30e78-705b-4a13-8229-467bf501b124" />

### Transactions Screen
<img width="497" alt="Transactions" src="https://github.com/user-attachments/assets/416bdafd-504c-4684-baf2-f051e15f9c55" />

### Login Registers Screen
<img width="497" alt="Login registers" src="https://github.com/user-attachments/assets/75ffec48-828f-4677-8bb8-926e86a5f7ac" />

---

## License

This project is for educational/portfolio purposes. See the `LICENSE` file for details.