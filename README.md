# PP PRINTER & Advertising – Accounting & ERP

![Logo](logo.webp)

Printing press aur advertising business ke liye ek single-file web app: bill se hisaab tak sab kuch aik jagah. Sales, quotations, delivery challan, purchase, expenses, bank aur cash book. Data Firebase Firestore ke zariye sab devices par live sync hota hai.

## Features

| Section | Modules |
|---|---|
| Overview | Dashboard |
| Sales | Customer Directory, Sales & Billing (Invoice), Quotations, Delivery Challan, Customer Ledgers / Account Statement |
| Stock & Kharcha | Purchase & Stock, Supplier Payments, Daily Expenses (category folders, vouchers) |
| Accounts | Bank & Cash Book, Trial Balance, Balance Sheet |
| System | Backup / Restore (JSON), User Management |

Extra: WhatsApp par invoice bhejna, print-friendly documents, Admin / Staff roles, offline fallback (localStorage backup).

## Tech stack

- Plain HTML + vanilla JavaScript (`index.html`, koi build step nahi)
- [Tailwind CSS](https://tailwindcss.com) (CDN), [Font Awesome](https://fontawesome.com) 6.4, Manrope font
- Firebase Firestore (`pp_printers_store/main_database`) for cloud sync

## Chalane ka tareeqa

1. Repo clone karein ya `index.html` aur `logo.webp` download karein.
2. `index.html` browser mein kholein (ya GitHub Pages / kisi static host par deploy karein).
3. Pehli login: username `admin`, password `admin123`.
   **Login ke foran baad Users section mein admin ka password badal dein.**

## Deploy (GitHub Pages)

Repo Settings → Pages → branch `main`, folder `/ (root)`. Custom domain use karni ho to root mein `CNAME` file banayein jis mein sirf aap ka domain likha ho.

## Data & backup

- Cloud: Firestore document `pp_printers_store/main_database`
- Local: browser `localStorage` (`pp_cloud_backup`) fallback ke taur par
- Manual: System → Backup se JSON export / import karein. Backup files ko repo mein commit na karein (`.gitignore` mein shamil hain).

## Security notes

- Firebase config client-side hota hai; asal hifazat Firestore Security Rules se hoti hai. Rules ko sirf authorized access tak mehdood rakhein.
- Default `admin123` password foran tabdeel karein.

## Contributing

Dekhein [CONTRIBUTING.md](CONTRIBUTING.md) aur [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
