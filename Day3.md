
# 🏭 Production Line Management System (Flask App)

This is a web-based internal tool for managing production lines at ADF Foods Limited. The system is built using **Python Flask** for the backend and **HTML/CSS with Bootstrap** for the frontend UI.

---

## 📌 Key Features

- **Add / Update Production Line**  
  Admins can:
  - Select a division from the dropdown.
  - Choose a production line type (e.g., ASSORTED).
  - Enter line capacity.
  - Set status (Active/Inactive).
  - Save the data to the database.

- **Production Line Display Table**
  - Dynamically displays all saved production lines.
  - Shows: Division, Line Type, Capacity, and Status.

---

## ⚙️ Tech Stack

- **Backend**: Flask (Python)
- **Frontend**: HTML5, CSS3, Bootstrap
- **Database**: Oracle DB / SQLite (via SQLAlchemy)
- **Tools Used**: Jinja2 templates, WTForms/Flask-WTF (if using form validation)

---

## 🧱 Flask Route Sample

```python
@app.route('/production-line', methods=['GET', 'POST'])
def production_line():
    if request.method == 'POST':
        division = request.form['division']
        line = request.form['line']
        capacity = request.form['capacity']
        status = request.form['status']

        # Add logic to insert into DB
        insert_production_line(division, line, capacity, status)

    lines = get_all_production_lines()
    return render_template('production_line.html', lines=lines)
```

---

## 📁 Folder Structure

```
/adf-foods/
│
├── app.py
├── templates/
│   └── production_line.html
├── static/
│   └── styles.css
├── models.py
├── database.py
└── README.md
```

---

## ✅ Status

This is the **initial production-ready UI** with form and table integration. Backend is connected for CRUD operations. Future improvements may include:
- Search and filter functionality
- Edit/Delete options for existing entries
- Role-based access control
