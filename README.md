https://beeboat-bee-boat.github.io/Budget/ - link to project
Budget Tracker v0.1 — Release Notes

A personal budget tracker built as a single-file PWA. No app store, no subscription, no ads. Just open the link and start tracking.

What it does

Budget Tracker helps you manage your monthly money — what's coming in, what's going out, what you owe, and what you're saving toward. Everything syncs across devices through Firebase and works offline as a PWA.

Features
💰 Monthly Budget
Set up income (salary, hourly, base + commission, freelance)
Organize spending into customizable categories and items
Smart onboarding recommends budgets based on your income and savings goal
Edit budgets anytime — changes sync to all future months automatically
↻ Recurring Expenses
Mark any expense as recurring with one tap
Choose Ongoing (rent, insurance) or Has a balance (loans, financing)
Balance items track remaining debt with optional APR and payoff estimates
Confirm payments monthly with a [Pay] button — nothing counts until you say so
Auto-completes when a balance hits $0
💳 Credit Cards
Track balances, limits, interest rates, and billing dates
Debt payoff planner with month-by-month simulation (6/12/18/24 month targets)
Automatic interest calculation using the avalanche method
Utilization tracking across all cards
👥 Group Expenses
Create groups, add members, split bills
Equal or custom splits with live validation
Settle up tracking with per-person balances
All group data stored locally — no account needed for group members
🎯 Goals
Save up goals (green) — track progress toward a savings target
Pay down goals (red) — track debt payoff progress
Goals link to your budget items and sync automatically when you confirm payments
Trophy case for completed goals with edit/restore/remove
📊 Trends
Charts — monthly income vs expenses over time
Transactions — searchable log with filters (type, source, payment method, time range)
Summary — year-to-date totals and top spending categories
🏦 Net Worth
Track bank accounts with monthly balances
Month-end close flow: review finances, sort surplus into accounts
Unassigned money pool for funds you haven't allocated yet
🔒 Accounts & Sync
Username + password login with deterministic sync codes
Data syncs across devices via Firebase Realtime Database
Export/import JSON backups
Change password, recover account with sync code
🎨 Themes
6 built-in themes: Bee (default), Ocean, Sunset, Midnight, Forest, Slate
One-tap switching in settings with instant preview
⚙️ Settings
Subscriptions tracker (auto-appears in recurring bills)
Customizable start month for budget history
Timezone setting
Storage monitor
Data tools: reset month, recalculate totals, clean group transactions
Technical Details
Single HTML file — no build tools, no dependencies, no server
PWA — installable on mobile, works offline
~250 KB total size
Firebase Realtime Database for cross-device sync
GitHub Pages hosting (free)
Known Limitations (v0.1)
Single-file architecture means no code splitting — the whole app loads at once
Charts require an internet connection (Chart.js loaded from CDN)
Group data is local-only (not synced via Firebase)
No multi-currency support
No receipt/photo attachments
No bank connection or auto-import
