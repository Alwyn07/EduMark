# EduMark 🎓
**College Mark Management System — v1.3**

A fully offline, single-file web app for managing student marks, classes, and results. No server. No install. Just open the HTML file and go.

---

## 🚀 Quick Start

```
1. Download  →  marksheet-app.html
2. Open      →  Double-click or drag into any browser
3. Login     →  Admin:   admin / admin123
                Student: CS101 / pass123
```

Zero setup. Zero dependencies.

---

## ✨ Features

### 🛡️ Admin Portal
- **Dashboard** — Live stats: total students, pass/fail counts, class average; filter by class
- **Classes** — Create, rename, delete classes grouped by department
- **Students** — Add/edit/remove students; search by name or roll no.; filter by pass/fail
- **Marks Entry** — Per-student modal with multi-exam support; live pass/fail hints per subject
- **Subjects** — Configure subject codes, names, max marks, and minimum pass marks
- **Admin Accounts** — Add/remove admin users with role-based access
- **Scan Marksheet** — Upload a marksheet image and extract marks visually

### 👨‍🎓 Student Portal
- **Overview** — Total marks, percentage, class rank, overall pass/fail status
- **Subject Marks** — Per-subject breakdown with progress bars
- **Exam History** — Switch between exams; compare results across terms

### 🔐 Auth System
- Separate login flows for Admin and Student
- 3-step guided student self-registration
- Admin registration support
- Remember Me — 30-day session persistence
- Auto-login on return visit

---

## 🛠️ Tech

| | |
|---|---|
| Stack | Vanilla HTML + CSS + JS |
| Storage | `localStorage` (browser) |
| Fonts | DM Serif Display, DM Sans (Google Fonts) |
| Backend | None |
| Dependencies | None |

---

## 📁 Structure

```
edumark/
└── marksheet-app.html    # Entire app — one file
```

---

## 🔑 Demo Credentials

**Admin**
| Username | Password |
|----------|----------|
| `admin` | `admin123` |

**Students**
| Roll No. | Password |
|----------|----------|
| `CS101` | `pass123` |
| `CS102` | `pass123` |
| `CS201` | `pass123` |
| `ECE101` | `pass123` |
| `MSC101` | `pass123` |

---

## ⚙️ Customisation

All config lives inside the `<script>` block at the bottom of the HTML file.

**Add a subject:**
```js
{ code: 'PHY', name: 'Physics', max: 100, pass: 35 }
```

**Add a class:**
```js
{ id: 'cls-5', name: 'BCA First Year', dept: 'Computer Applications' }
```

**Add a student directly:**
```js
{ roll: 'BCA101', name: 'Your Name', classId: 'cls-5', password: 'pass123', marks: [] }
```

Or use the Admin UI — changes persist to `localStorage` automatically.

---

## 📦 Data Persistence

All data stored in browser `localStorage` under these keys:

| Key | Contents |
|-----|----------|
| `em_db` | Students + marks |
| `em_subjects` | Subject config |
| `em_classes` | Class list |
| `em_admins` | Admin accounts |
| `em_sess` | Active session |

> ⚠️ Clearing browser storage resets the app to demo defaults. Export/backup not yet built in — see Roadmap.

---

## 🔮 Roadmap

- [ ] Export marks to PDF / Excel
- [ ] Data backup & restore (JSON export)
- [ ] Dark mode
- [ ] Print-ready marksheet layout
- [ ] Bulk student import via CSV
- [ ] Parent portal (view-only)

---

## 🤝 Contributing

Issues and PRs welcome. This is a single-file project — keep it that way.

---
---

> *Built to make mark management simple for every college, not just the ones with IT departments.*