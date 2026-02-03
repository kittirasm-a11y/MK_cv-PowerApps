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
## 🔗 Live Application

You can access the live Power Apps application here:

👉 **[Open MK_cv Power Apps Application]https://apps.powerapps.com/play/e/default-aaf7688a-f496-40d1-bd44-3cabbe690ba0/a/716039af-6868-4f65-a33e-0646bf500a84?tenantId=aaf7688a-f496-40d1-bd44-3cabbe690ba0&hint=e6610002-5b8e-4683-9df8-1781411f2d42&sourcetime=1770120902005

> ⚠️ Note: Access requires a European University Cyprus Microsoft account.

