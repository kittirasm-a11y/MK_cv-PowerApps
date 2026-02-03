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

---

### 🧑‍💼 Work Experience
The Work Experience section presents professional roles using a dynamic gallery connected to a SharePoint list.
Key features:
- Displays company, position, duration, and description
- Data stored and retrieved from Microsoft Lists (SharePoint)
- Search functionality for filtering work entries
- Form-based input to add new work experience entries

---

### 🎯 Interests & Hobbies
The Interests & Hobbies section allows users to select personal interests and view contextual details.
Key features:
- Radio button selection (Sports, Music, Coding, Travel)
- Toggle switch to show/hide additional details
- Dynamic content displayed based on selection

---

### 🧠 Interactive Quiz
The application includes an interactive quiz that tests user knowledge about the CV owner.
Key features:
- Multiple-choice questions
- Randomized answer order using collections
- Score calculation in percentage
- Clear/reset functionality

---


## Author
### 🧑‍🎓 Author

**Markos Kittiras**  
B.Sc. Computer Information Systems  
European University Cyprus  

Course: Smart Phone Programming  
Technology: Microsoft Power Apps (Canvas App)

---

## Sources & References
### 📚 Sources & References

- Microsoft Power Apps Documentation  
  https://learn.microsoft.com/power-apps/

- Power Fx Formula Reference  
  https://learn.microsoft.com/power-platform/power-fx/

- Microsoft Lists (SharePoint Integration)  
  https://learn.microsoft.com/microsoft-365/lists/

  ## 🔗 Live Application

You can access the live Power Apps application here:

👉 **[Open MK_cv Power Apps Application]https://apps.powerapps.com/play/e/default-aaf7688a-f496-40d1-bd44-3cabbe690ba0/a/716039af-6868-4f65-a33e-0646bf500a84?tenantId=aaf7688a-f496-40d1-bd44-3cabbe690ba0&hint=e6610002-5b8e-4683-9df8-1781411f2d42&sourcetime=1770120902005

---

**Example Power Fx:**
```powerfx
If(
    Toggle1.Value = true,
    Filter(CourseInfo, Semester = "Fall"),
    Filter(CourseInfo, Semester = "Spring")
)




