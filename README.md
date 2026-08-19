# BetterBudget

Smart budgeting for people who want to get ahead.

**Live app:** [beeboat-bee-boat.github.io/Budget](https://beeboat-bee-boat.github.io/Budget/)

---

## Getting Started

### First time
1. Open the link above on your phone or computer
2. Tap **Sign in with Google** or **Get started without an account**
3. Follow the 4-step setup: income → categories → budget → credit cards
4. You're in — start logging expenses

### Adding to your home screen (recommended)
- **iPhone:** Safari → Share button → Add to Home Screen
- **Android:** Chrome → three dots → Add to Home Screen

---

## How to Use It

### Daily (30 seconds)
Tap **+ Add** in the top right whenever you spend or earn money.

- **Expense** — pick category, item, amount, and how you paid
- **Income** — pick source, amount, and where to deposit it
- **Payment** — log a credit card payment
- **Deposit** — move money into an account

If a category, item, card, or account doesn't exist yet, tap the **+ button** inside any picker to create one on the spot. You'll go right back to where you were.

### Weekly (2 minutes)
1. Open the app and review your **dashboard** — check the spending breakdown and recent transactions
2. Go to **Money Out** and tap **[Pay]** on any recurring bills you've paid this week
3. Check **Alerts** in the More tab for anything that needs attention

### Monthly (5 minutes)
1. On the last day of the month, tap **Close [Month]** on the dashboard
2. Walk through the checklist — confirm income, expenses, card balances
3. Review any alerts that pop up (you can still close with warnings)
4. Sort your surplus into accounts if you have extra money
5. The month locks and a new one starts with your recurring items ready to go

---

## Features at a Glance

### Dashboard
Your home base. Shows:
- Money In / Money Out / Saved this month
- Net for the month (green = positive, red = negative)
- Spending breakdown with category bars
- Recent transactions
- Bills due (unpaid recurring items)
- Group activity (if you have groups)

### Money In / Money Out
Tap the dashboard cards to see details. Each category expands to show items with budgeted vs actual amounts. Tap any amount to edit. Tap **Edit** to rearrange or delete items.

### Credit Cards
See all your cards with balances, utilization, and interest charges. The **payoff planner** shows a month-by-month timeline of how to become debt-free using the avalanche method (highest APR first).

### Groups
For splitting expenses with roommates, friends, or coworkers.
1. Create a group → share the code
2. Add members
3. Log shared expenses → pick who paid and how to split
4. Settle up when someone pays their share — the app tracks what it was for
5. History shows every expense and settlement in one log

### Goals
Set savings targets or payoff goals. Track progress with color-coded cards. Complete them and they move to your trophy case.

### Trends
- **Charts** — spending by category, income vs spending, monthly breakdown
- **Transactions** — searchable log of everything with filters
- **Summary** — year-to-date totals
- **Financials** — (accountant mode only) Income Statement, Balance Sheet, Journal Entries, Variance Report

### Alerts
The app watches for problems and tells you how to fix them:
- Budget overages above your threshold
- Card utilization above your target percentage
- Unpaid recurring bills
- Negative account balances
- Spending exceeding income

Each alert includes the numbers and exactly where to go to fix it.

### More (Settings)
- **Profile** — sign in/out, link Google account
- **Appearance** — accountant mode, currency, themes
- **Budget Setup** — take the tour, start month, timezone, default payment method
- **Alerts** — threshold settings
- **Subscriptions** — track recurring subscriptions with monthly/annual totals
- **Net Worth** — bank accounts and balances
- **Data** — sync, export (JSON/CSV), import, reset
- **Danger Zone** — edit setup (keeps data) or start over (deletes everything)

---

## Accountant Mode

Toggle it on in More → Appearance. Everything relabels to real accounting terms. A **Financials** tab appears under Trends with:

- **Income Statement** — your personal P&L
- **Balance Sheet** — assets minus liabilities = equity
- **Journal Entries** — every transaction as a debit/credit pair with account numbers
- **Budget Variance Report** — budgeted vs actual with percentage variance

Great for anyone learning accounting terminology or prepping for finance conversations.

---

## Syncing Across Devices

Sign in with the same Google account on any device to access your data. The app syncs in real time when both devices are online.

If you edited offline, the app compares timestamps and keeps the newer version when you come back online.

Tap **More → Data → Sync data now** to force a sync.

---

## Exporting Your Data

Two options in More → Data (or Trends → Transactions):

- **Export JSON** — full backup, can be imported back into BetterBudget
- **Export CSV** — spreadsheet-friendly, opens in Excel/Google Sheets/Numbers

The CSV includes all transactions, card balances, account balances, and subscriptions.

---

## Updating the App

The app updates automatically when you open it — no app store needed. We recommend **opening the app at least once a week** to stay on the latest version.

If you think you're on an old version:
- **Desktop:** Ctrl+Shift+R (hard refresh)
- **iPhone:** Settings → Safari → Advanced → Website Data → find github → Delete
- **Android:** Chrome → three dots → Settings → Privacy → Clear browsing data → Cached images and files

Check your version at the bottom of the More tab.

---

## Updating the Code (for developers)

The entire app is a single `index.html` file hosted on GitHub Pages.

### To push an update:
```bash
cd your-repo
# Replace index.html with the new version
cp ~/path/to/new/index.html ./index.html
git add index.html
git commit -m "v1.x — description of changes"
git push
```

GitHub Pages deploys automatically within a few minutes. Users get the update on their next visit thanks to the no-cache meta tags.

### Recommended update cadence:
- **Weekly** — push bug fixes and small improvements
- **Biweekly** — push new features
- **Always** — test in incognito before pushing to make sure it works clean

### Before pushing:
1. Check syntax: open the file in a browser, check the console for errors
2. Test onboarding: incognito window → sign in → complete setup
3. Test quick-add: log an expense, income, payment
4. Check mobile: open on your phone and tap through the main flows

---

## Tech Stack

- Single HTML file (HTML + CSS + JS, no build step)
- Firebase Realtime Database (data storage)
- Firebase Auth (Google Sign-In)
- GitHub Pages (hosting)
- Chart.js (lazy-loaded for trends)
- Inter font (Google Fonts)

---

## Support

Found a bug? Open an issue on the GitHub repo or just fix it in `index.html` and push.
