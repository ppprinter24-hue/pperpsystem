# Project guide

PP PRINTER & Advertising – Accounting & ERP. Single-file app: `index.html` (HTML + CSS + vanilla JS, Tailwind via CDN, Firebase Firestore sync).

## Rules for working here

- Sara code `index.html` mein hai; koi build step nahi.
- Data shape `blank()` function mein define hai (`users`, `customers`, `sales`, `quotations`, `purchases`, `expenses`, `bankTransfers`, ...). Naye fields add karte waqt purane backups ke saath compatibility rakhein.
- Saari saved text `esc()` se escape karein.
- Credentials, Firebase keys ya real business data naye files mein commit na karein.
- Hisaab ke logic (`entries()`, `calc()`, ledger, trial balance) badalne par numbers dobara verify karein.
