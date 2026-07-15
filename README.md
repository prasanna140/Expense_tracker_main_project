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
Expense-Tracker/
│
├── index.html
├── README.md
├── .gitignore
├── LICENSE
│
├── assets/
│   ├── images/
│   │   ├── logo.png
│   │   ├── dashboard.png
│   │   ├── profile.png
│   │   ├── empty-state.svg
│   │   └── icons/
│   │       ├── income.svg
│   │       ├── expense.svg
│   │       ├── wallet.svg
│   │       ├── chart.svg
│   │       └── user.svg
│   │
│   └── favicon/
│       └── favicon.ico
│
├── css/
│   ├── style.css
│   ├── variables.css
│   ├── navbar.css
│   ├── dashboard.css
│   ├── transactions.css
│   ├── analytics.css
│   ├── forms.css
│   ├── modal.css
│   ├── profile.css
│   ├── darkmode.css
│   └── responsive.css
│
├── js/
│   ├── app.js
│   ├── router.js
│   ├── storage.js
│   ├── data.js
│   ├── utils.js
│   ├── charts.js
│   ├── validation.js
│   ├── theme.js
│   │
│   ├── auth/
│   │   ├── login.js
│   │   ├── register.js
│   │   └── authGuard.js
│   │
│   ├── components/
│   │   ├── navbar.js
│   │   ├── sidebar.js
│   │   ├── footer.js
│   │   ├── modal.js
│   │   ├── toast.js
│   │   ├── transactionCard.js
│   │   └── summaryCard.js
│   │
│   ├── pages/
│   │   ├── dashboard.js
│   │   ├── transactions.js
│   │   ├── analytics.js
│   │   ├── profile.js
│   │   └── settings.js
│   │
│   └── services/
│       ├── transactionService.js
│       ├── categoryService.js
│       └── userService.js
│
├── pages/
│   ├── login.html
│   ├── register.html
│   ├── dashboard.html
│   ├── transactions.html
│   ├── analytics.html
│   ├── profile.html
│   └── settings.html
│
├── data/
│   ├── categories.json
│   └── sampleData.json
│
└── docs/
    ├── screenshots/
    │   ├── login.png
    │   ├── dashboard.png
    │   ├── transactions.png
    │   ├── analytics.png
    │   ├── profile.png
    │   └── darkmode.png
    │
    ├── project-report.pdf
    └── architecture.png

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
