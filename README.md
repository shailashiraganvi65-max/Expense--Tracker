# 💰 Expense Tracker (Full Stack)

A simple full-stack Expense Tracker application built using **Express.js**, **SQLite (better-sqlite3)**, and **React + Vite**.

The application allows users to:

- Add expenses
- View expenses with pagination
- Filter expenses by category
- Delete expenses
- View monthly spending summary grouped by category
- Store all data locally using SQLite

---

# Tech Stack

## Backend

- Node.js
- Express
- CORS
- SQLite
- better-sqlite3

## Frontend

- React
- Vite
- CSS

---

# Project Structure

```
project-folder/
│
├── backend/
│   ├── index.js
│   ├── package.json
│   └── data.db
│
└── frontend/
    ├── src/
    │   ├── App.jsx
    │   ├── App.css
    │   └── main.jsx
    └── ...
```

---

# Features

## Expense Management

- Add new expense
- Title validation
- Positive amount validation
- Select category
- Select expense date

---

## Expense List

- View all expenses
- Pagination support
- Category filtering
- Delete expenses
- Latest expenses displayed first

---

## Monthly Summary

- Month selector
- Total spending by category
- Horizontal summary bars
- Grand total calculation

---

## Database

SQLite database automatically creates an **expenses** table with the following fields:

| Column | Type |
|---------|------|
| id | INTEGER |
| title | TEXT |
| amount | REAL |
| category | TEXT |
| date | TEXT |
| created_at | TEXT |

---

# API Endpoints

## Create Expense

**POST**

```
/expenses
```

Example Request

```json
{
  "title": "Groceries",
  "amount": 450.50,
  "category": "Food",
  "date": "2026-07-06"
}
```

---

## Get Expenses

**GET**

```
/expenses
```

Supports query parameters:

```
?page=1
&limit=10
&category=Food
&month=2026-07
```

Example

```
GET /expenses?page=1&limit=10
```

---

## Monthly Summary

**GET**

```
/expenses/summary
```

Example

```
GET /expenses/summary?month=2026-07
```

---

## Update Expense

**PUT**

```
/expenses/:id
```

Example

```json
{
  "title": "Fuel",
  "amount": 800
}
```

---

## Delete Expense

**DELETE**

```
/expenses/:id
```

Example

```
DELETE /expenses/5
```

---

# Categories

The application supports the following categories:

- Food
- Transport
- Bills
- Entertainment
- Other

---

# Running the Backend

Open a terminal inside the **backend** folder.

Start the server:

```bash
node index.js
```

Server runs at:

```
http://localhost:5000
```

---

# Running the Frontend

Open another terminal inside the **frontend** folder.

Start the Vite development server:

```bash
npm run dev
```

Open the URL displayed in the terminal (usually):

```
http://localhost:5173
```

---

# How It Works

### Adding an Expense

1. Enter title
2. Enter amount
3. Select category
4. Choose date
5. Click **Add Expense**

The expense is saved in SQLite and immediately appears in the list.

---

### Viewing Expenses

The application displays:

- Expense title
- Category
- Amount
- Date

Expenses are sorted by newest date first.

---

### Filtering

Use the category dropdown to filter expenses.

Available filters:

- All Categories
- Food
- Transport
- Bills
- Entertainment
- Other

---

### Pagination

The expense list supports:

- Previous page
- Next page
- Current page indicator

---

### Monthly Summary

Choose a month to view:

- Spending grouped by category
- Visual summary bars
- Grand total spending

---

# Validation

The application validates:

- Title is required
- Amount must be greater than zero
- Category is required
- Date is required

Invalid data returns appropriate error messages.

---

# Database

The SQLite database file is:

```
backend/data.db
```

It is automatically created on first run.

---

# Default Ports

Backend:

```
5000
```

Frontend (Vite):

```
5173
```

---

# Technologies Used

- Express.js
- React
- Vite
- SQLite
- better-sqlite3
- JavaScript
- CSS

---

# Future Improvements

- Edit existing expenses from the UI
- Search expenses by title
- Export expenses to CSV
- Charts and analytics
- Dark mode
- Budget tracking
- Monthly spending trends

---

# Author

Expense Tracker Project

Built using **Express.js**, **SQLite**, and **React + Vite**.
