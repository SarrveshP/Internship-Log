# 🧾 IT Budget Management System – Day Report & Learning Log

---
# Day 2 Report  

**Intern Name:** Sarvesh Patil  
**Date:** 04/06/25  
**Department:** IT Department  
**Supervisors:** Abhishek  

---
## 🧠 Learning Intent
> *"This is the exoskeleton of the code framework, which is properly integrated with the organization’s software environment. It reflects a practical learning implementation that I am sharing as part of my real-world development practice."*

---

## ✅ Activities Completed in a Day

| **Area**                 | **Task** |
|---------------------------|----------|
| 📋 **Planning & Specification** | - Defined complete module specification.<br>- Finalized entities: Budget Master, Transaction Master.<br>- Outlined access control and reports. |
| ⚙️ **Framework & Setup** | - Selected Flask + SQLite for backend and HTML/CSS/Bootstrap for frontend.<br>- Initialized Flask app with modular structure. |
| 🧱 **Modeling & DB Integration** | - Created SQLAlchemy models: `IT_BUDGET_MASTER`, `IT_BUDGET_TRANSACTIONS`.<br>- Created database with proper indexing. |
| 🧾 **Form Creation** | - Built `BudgetForm` using Flask-WTF with editable fields.<br>- Connected to SQLite for insertion and retrieval. |
| 🧪 **Debugging & Testing** | - Fixed Save button issues and validated form data.<br>- Printed error logs, ensured seamless data population. |
| 🎨 **Frontend Design** | - Designed responsive forms using Bootstrap.<br>- Added dynamic table to show submitted data in real-time. |
| 📘 **Documentation** | - Wrote detailed `README.md` for developers and deployment.<br>- Created day learning report (this log). |

---

## 📚 Key Learnings
- ✅ How to translate a real-world use case into technical modules and DB schema.  
- ✅ Practical application of Flask-WTF forms with SQLAlchemy ORM.  
- ✅ Fixing end-to-end CRUD flow: form → validation → database → render.  
- ✅ Debugging and inspecting form validation errors.  
- ✅ Writing clean, structured project documentation (`README.md`).  
- ✅ Preparing for integration with enterprise environments like Oracle DB, role-based access, etc.  

---

## 🧭 Next Steps
- Implement **budget limit validation** (to restrict over-utilization).  
- Create a **live KPI dashboard**.  
- Add **report visualizations** (category-wise, monthly trends).  
- Integrate **login and roles** (Admin vs Division Head).  
- Move from SQLite to **Oracle** for production compatibility.  
