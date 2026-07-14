# ExpenseWise

A refined, single-page expense tracker for your everyday finances — sign up, log in, add income/expense transactions, filter and search them, see category breakdowns, and manage your profile, all with a light/dark theme. Your data is stored only in your browser (`localStorage` / `sessionStorage`) — nothing is sent to a server.

This repository contains the **modular** version of the original single-file `Expense_Wise.html` build. The site's design, functionality, layout, and behavior are **100% unchanged** — only the code organization has changed, splitting one large HTML file into clearly separated HTML, CSS, and JavaScript modules.

## Features
- Email/password sign up & login (stored locally, per-browser)
- Password strength meter with live rule checklist
- Session restore (stay logged in on refresh)
- Add, edit, and delete income/expense transactions
- Inline edit form on wide screens, edit modal on narrow screens
- Filter transactions by month, today, this week, or a custom date range
- Search transactions by category, note, amount, or type
- Category breakdown bar chart for expenses
- Editable user profile: name, email, password, and avatar photo
- Light/dark theme toggle with saved preference
- Fully responsive layout

## Project Structure
ExpenseWise/
│
├── index.html              # Main HTML entry point
├── README.md
├── LICENSE
│
├── assets/
│   ├── images/              # Static images (none required by default build)
│   └── fonts/                # Custom fonts (the app uses system/Georgia serif fonts by default)
│
├── css/
│   ├── variables.css        # CSS custom properties (light & dark theme tokens)
│   ├── global.css           # Resets, body background, layout wrapper, toast, scrollbar, footer
│   ├── auth.css              # Auth screen: card, tabs, brand, mascot, auth footer
│   ├── navbar.css            # Top bar: avatar, nav tabs, theme toggle, logout button
│   ├── dashboard.css         # Summary cards, panels, generic card, month nav, category breakdown
│   ├── transaction.css       # Filter bar, search bar, transaction list & items
│   ├── profile.css           # Profile page avatar & section styling
│   ├── modal.css             # Edit-transaction modal overlay & box
│   ├── forms.css             # Shared form fields, password strength UI, buttons, type toggle
│   ├── responsive.css        # Media query breakpoints
│   └── dark-theme.css        # Dark-mode specific selector overrides
│
├── js/
│   ├── app.js                # Global app state + DOMContentLoaded bootstrap / session restore
│   ├── auth.js                # Tab switching, password visibility, signup & login handlers
│   ├── session.js             # Session start, logout, enter-app, identity refresh
│   ├── storage.js             # localStorage helpers (users + per-user transaction data)
│   ├── theme.js                # Light/dark theme apply, toggle, and init
│   ├── profile.js              # Avatar upload & profile save handlers
│   ├── dashboard.js            # Dashboard ↔ Profile view navigation
│   ├── transaction.js          # Add/edit/delete transactions (inline form) + list rendering
│   ├── filters.js              # Date filter mode logic, month navigation, filtering helper
│   ├── category.js             # Category select population + category breakdown rendering
│   ├── summary.js              # Summary cards rendering + renderAll() orchestrator
│   ├── modal.js                 # Edit-transaction modal open/close/save (small screens)
│   ├── validation.js            # Password strength calculation + strength UI feedback
│   ├── utils.js                  # Generic utilities (toast, money formatting, email check, dates)
│   └── constants.js              # Storage keys and category definitions
│
├── data/
│   └── sample-data.json      # Example transaction data shape (for reference only — the app itself reads/writes localStorage, not this file)
│
├── docs/
│   ├── screenshots/          # Place UI screenshots here
│   ├── project-report.pdf    # Optional project write-up
│   └── architecture.png      # Optional architecture diagram
│
└── .gitignore

## How to Run
1. Download or Clone the repository.
2. Open the project folder.
3. Double-click **index.html**
OR
Open using VS Code and install **Live Server**.
Right click on **index.html**
Click **Open with Live Server**

## How It Works
### Authentication
- Users can register with their email.
- Passwords are validated before account creation.
- Login sessions are stored using Session Storage.

### Transactions
Users can:
- Add Income
- Add Expenses
- Edit Transactions
- Delete Transactions
All transactions are stored in Local Storage.

### Filters
Users can filter transactions by:
- Month
- Today
- Current Week
- Custom Date Range

### Profile
Users can:
- Update Name
- Update Email
- Change Password
- Upload Profile Image

### Theme
Supports:
- Light Mode
- Dark Mode
Theme preference is saved automatically.

## Data Storage
The application stores information locally inside the browser using:
- LocalStorage
- SessionStorage
No external database is required.

## Browser Compatibility
- Google Chrome
- Microsoft Edge
- Firefox
- Brave
- Opera

## Future Improvements
- Export transactions to PDF
- Export transactions to Excel
- Charts using Chart.js
- Budget Goals
- Email Verification
- Cloud Database Integration
- Multi-device Sync
## Screen shots
![image alt](https://github.com/prasanna140/Expense_tracker_main_project/blob/22dff8818a4ae866958b4aa1bef611b1c06d31d4/Expense_tracker_showcases.png)
