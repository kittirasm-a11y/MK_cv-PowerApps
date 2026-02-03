# MK_cv – Interactive CV (Power Apps)

MK_cv is an interactive CV built using **Microsoft Power Apps (Canvas App)**.
The application presents academic background, work experience (NOT REAL), interests, and an interactive quiz through a clean, multi-screen interface.

> ⚠️ Note: Due to university tenant restrictions (European University Cyprus), direct app export
> (.msapp / solutions) is disabled. This repository documents the application through screenshots
> and extracted Power Fx logic.

---

## Features

### 🏠 Home Page
- Personal introduction
- Navigation buttons to all sections
- Clean, CV-style layout

---

### 🎓 Academic Achievements
- Courses displayed dynamically using galleries
- Semester-based filtering (Spring / Fall)
- Course details (Grade, ECTS) shown on selection

**Example Power Fx:**
```powerfx
If(
    Toggle1.Value = true,
    Filter(CourseInfo, Semester = "Fall"),
    Filter(CourseInfo, Semester = "Spring")
)
