# BetterBudget v1.0 — Release Notes

**Ship date:** August 19, 2026
**Live:** [beeboat-bee-boat.github.io/Budget](https://beeboat-bee-boat.github.io/Budget/?v=3)

---

## What is it

BetterBudget is a personal finance PWA built as a single HTML file. No backend, no subscription, no ads. Sign in with Google to sync across devices, or use without an account.

Built for people who want to actually understand where their money goes — and for sales reps who want to learn how closing the books works by doing it with their own finances.

---

## Core Features

### Budgeting
- Monthly budget with Money In / Money Out tracking
- Recurring expenses with [Pay] confirmation — nothing counts until you say it happened
- Dashboard with spending breakdown, recent transactions, bills due, and group activity
- Savings rate, spending velocity, and running total across months
- Close the month with a checklist, sort surplus into accounts, lock the period

### Quick Add
- Persistent [+ Add] button in the header on every page
- 4 tabs: Expense, Income, Payment, Deposit — always accessible
- Inline creation everywhere: new categories, items, income sources, cards, accounts — without leaving your flow
- Cancel on sub-modals returns to quick-add with all inputs preserved

### Credit Cards
- Track balances, limits, APR, minimum payments, statement dates
- Payoff planner with month-by-month projections (avalanche method)
- Timeline picker: 6 / 12 / 18 / 24 / custom months
- Interest calculations with real amortization math

### Groups
- Create groups, add members, split expenses
- Equal or custom split amounts with live validation
- "Who paid?" selector — track when others pay, not just you
- Settle up with full context of what expenses were covered
- Transaction history with expenses and settlements in one log
- Dashboard card showing who owes you (green) and who you owe (red)

### Goals
- Savings goals (saving toward a target) and payoff goals (paying down a balance)
- Color-coded: green for saving, red for paying off
- Trophy case for completed goals

### Trends
- Charts: by category, income vs spending, this month breakdown
- Transaction log: searchable, filterable by type / source / method / time
- Summary: year-to-date overview
- CSV and JSON export right from the Transactions tab

### Alerts
- Budget overages, card utilization, unpaid recurring bills, negative accounts, spending > income
- Each alert includes what's wrong, the numbers, and exactly where to go to fix it
- Customizable thresholds: dollar amount for budget overages, percentage for card utilization
- Toast notification with [View] button after any transaction that triggers an alert
- Alerts surface in the Close Month checklist as warnings (proceed with "Close anyway")

---

## Accountant Mode

Toggle in More > Appearance. Swaps all labels to real accounting terminology and adds a Financials tab under Trends.

| Standard | Accountant Mode |
|---|---|
| Budget | General Ledger |
| Money In | Revenue Recognition |
| Money Out | Operating Expenses |
| Close Month | Close Period |
| Groups | Entities |
| Owed to you | Accounts Receivable |
| You owe | Accounts Payable |
| Spending breakdown | Cost Center Analysis |
| Net Worth | Statement of Net Position |

### Financial Statements (Accountant Mode only)
- **Income Statement** — Revenue, Operating Expenses, Net Income with margin %
- **Balance Sheet** — Assets, Liabilities, Equity with account numbers
- **Journal Entries** — Every transaction shown as DR/CR with account codes
- **Budget Variance Report** — Budget vs Actual with dollar and percentage variance

---

## Auth & Sync

- **Google Sign-In** via Firebase Auth — one tap, works across devices
- **Local mode** — get started without an account, link Google later
- **Timestamp-based conflict resolution** — newer version wins when syncing across devices
- **Local backup** — data always saved to localStorage alongside Firebase
- **Save safety** — saves on visibility change, tab switch, beforeunload, and pagehide

---

## Design

- Inter font, dark navy/purple theme (midnight default)
- 6 themes: midnight, bee, ocean, sunset, forest, mono
- Sticky header with context buttons + permanent [+ Add]
- Bottom sheet modals with slide-up animation (no replay on re-render)
- Scroll position and input values preserved across modal interactions
- 44px minimum touch targets, number input validation (no letters, 2 decimal max)
- Lazy-loaded Chart.js, memoized calculations, requestAnimationFrame render batching

---

## Onboarding

1. **Income** — salary, hourly, base + commission, freelance, commission only
2. **Categories** — pick from suggestions or create custom, including Loans
3. **Budget plan** — suggested allocations, debt items auto-detected with balance + APR fields
4. **Credit cards** — add with balance, limit, APR, min payment, statement date
5. **Walkthrough** — 7-step guided tour of the app

Re-onboarding (More > Edit setup) preserves all transaction history.

---

## Technical

- Single HTML file, 4,779 lines, 302 KB
- Firebase Realtime Database + Firebase Auth (Google Sign-In)
- No build step, no dependencies, no npm
- GitHub Pages hosting
- No-cache meta tags for instant updates
- CSV export/import for data portability
