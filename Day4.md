# 💰 Budget Transactions & Reporting System (Web App)

This is a web-based financial management tool for tracking budget allocations and transactions across multiple divisions. The system is built using **HTML/CSS/JavaScript** for the frontend with **client-side storage**.

---

## 📌 Key Features

- **Transaction Management**  
  Users can:
  - Select from budget-enabled categories
  - Enter transaction amounts with real-time budget validation
  - Choose from multiple divisions (Mumbai, Gujarat, etc.)
  - Add purpose notes and track entered-by information

- **Interactive Dashboard**
  - Real-time summary tiles showing:
    - Amount Available
    - Amount Remaining
    - Total Allocated
  - Filterable transaction history table
  - Visual charts for spending analysis

---

## ⚙️ Tech Stack

- **Frontend**: HTML5, CSS3, JavaScript (ES6)
- **Data Visualization**: Chart.js
- **Data Persistence**: localStorage API
- **Export Tools**: SheetJS (Excel), jsPDF (PDF reports)
- **UI Framework**: Pure CSS with custom design system

---

## 🧱 Core JavaScript Sample

```javascript
// Handle transaction submission
document.getElementById("transactionForm").addEventListener("submit", function(e) {
  e.preventDefault();
  
  const formData = {
    id: Date.now(),
    category: document.getElementById("category").value,
    amount: parseFloat(document.getElementById("amount").value),
    division: document.getElementById("division").value,
    purpose: document.getElementById("purpose").value,
    entered_by: document.getElementById("entered_by").value,
    date: new Date().toLocaleDateString()
  };

  // Budget validation
  const availableBudget = categoryBudgets[formData.category].amount;
  if (formData.amount > availableBudget) {
    showAlert("Error: Amount exceeds available budget", "danger");
    return;
  }

  // Save transaction
  transactionData.push(formData);
  localStorage.setItem("transactionData", JSON.stringify(transactionData));
  updateDashboard();
});
```
## File Management :
```
/budget-system/
│
├── index.html
├── styles/
│   └── main.css
├── scripts/
│   ├── app.js
│   ├── charts.js
│   └── reports.js
├── assets/
│   ├── icons/
│   └── templates/
└── README.md
```
