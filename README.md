# SmartBudgetManagger
A project for managing Budget.
Documentation

1.1 Audience profile:

1-who will use the workbook : -

Small business employees, freelancers,

or individual users looking to manage personal and
monthly operational income and expenses.

2-Expected level of Excel knowledge:
-Basic/Beginner: Users understand basic data entry .

3-Tasks to perform:
-Enter daily income and expenses.

-Select transaction types and categories from drop-
down lists.

-Set and edit category budget limits.

4-Terms that may be difficult:
Conditional Formatting, SUMIFS, Data Validation, and

dynamic sheet references.

Documentation

5-Problems they might encounter:
-Overwriting dynamic cell formulas (e.g.,
modifying the automated Month column in

Transactions).

-Inputting incorrect dates or text into numerical

amount fields.

-Forgetting to select a category, leading to
unassigned budget calculations on the
Dashbord

6- Reading behavior:
Users will scan quickly while working. They
need clear step-by-step numbered steps, callout
warnings, and annotated screenshots rather

than long paragraphs
README: SmartBudget Manager
Track your income and expenses in Excel and see at a glance whether you are within your budget.
What it does
• Records monthly income and expenses in one table.
• Sorts expenses into categories (Food, Transport, Rent, Health, Education).
• Calculates your monthly balance automatically.
• Shows a pie chart of expenses by category.
• Warns you with OVER BUDGET when your spending is higher than your budget.
What you need
• Microsoft Excel 2016, 2019, 2021 or Microsoft 365 (or a compatible spreadsheet program).
• The file SmartBudget_Manager.xlsx. No internet, macros or add-ins are required.
What's in the package
File Use it to...
SmartBudget_Manager.xlsx Track your budget (the product).
SmartBudget_User_Guide_lmm_GroupX.pdf Follow step-by-step instructions with screenshots.
Software_Requirements_SmartBudget_lmm_GroupX.pd
f

See what the workbook must do and its limits.

Get started in 5 steps
1. Open SmartBudget_Manager.xlsx. If Excel shows Protected View, click Enable Editing.
2. Open the Categories sheet and set your monthly budget for each category (column Monthly Budget).
3. Open the Transactions sheet. In the first empty row enter the date, a description and choose the Type.
4. For an expense, choose a Category and type the amount in the Expense column. For income, type it in the
Income column.
5. Open the Dashboard to read your totals, balance, chart and budget status. Press Ctrl+S to save.
Quick example
Enter Date 2026-09-10, Description Electricity bill, Type Expense, Category Rent, Expense 60. The Dashboard total
expenses rise by 60 and the monthly balance falls by 60.
Good to know
• Do not type in the Month column or on the Dashboard: they calculate by themselves.
• Up to 47 transactions (rows 4 to 50) are counted. Use one copy of the file per month.
• Pick categories from the drop-down list so every expense appears in the chart.
Software Requirements: SmartBudget Manager
Document version 1.0 | Product: SmartBudget_Manager.xlsx | Prepared by lmm, October 2026
1. Document purpose
This document states what SmartBudget Manager must do and the qualities it must have. It is the reference for the README and the
User Guide, and lets readers check that the documentation matches the product.
2. Product overview
SmartBudget Manager is an Excel workbook that records monthly income and expenses, groups expenses by category, calculates the
balance automatically, shows a chart of expenses by category and warns the user when the budget limit is exceeded. It uses SUM,
SUMIFS, IF, a pie chart and conditional formatting. It has three worksheets:
Worksheet Purpose
Dashboard Shows total income, total expenses, monthly balance, budget status, the category summary and the chart.
Transactions Lets the user enter income and expenses (Date, Description, Type, Category, Income, Expense, Notes; Month is

automatic).

Categories Holds the expense categories (Food, Transport, Rent, Health, Education) and a monthly budget for each.
3. Target users
Beginner-level Excel users who manage a personal, student or very small household budget (see the Audience Profile). No accounting
or formula skills are assumed.
4. Functional requirements
ID The workbook shall... Where
FR1 let the user record income (date, description, amount) with Type = Income. Transactions
FR2 let the user record expenses (date, description, amount) with Type = Expense. Transactions
FR3 offer drop-down lists for Type (Income, Expense) and Category (from the Categories sheet). Transactions
FR4 fill the Month column automatically (format yyyy-mm) from the date. Transactions
FR5 calculate Total Income, Total Expenses and Monthly Balance (income minus expenses) automatically. Dashboard
FR6 calculate the actual expense and the remaining budget for each category (SUMIFS). Dashboard
FR7 display a pie chart titled "Expenses by Category". Dashboard
FR8 let the user change the monthly budget of each category; the overall budget is their sum. Categories
FR9 show WITHIN BUDGET (green) or OVER BUDGET (red) when total expenses are below or above the overall
budget.

Dashboard

5. Non-functional requirements
• Usability: adding a transaction takes no more than 8 steps; every sheet has clear titles and short on-sheet guidance.
• Compatibility: works in Microsoft Excel 2016, 2019, 2021, Microsoft 365 or a compatible program; no macros or add-ins.
• Reliability and performance: results update immediately after each entry; formulas stay visible and traceable.
• Privacy: data stays in the local file; no internet connection or account is needed.
• Readability: status is shown by words as well as colour; amounts use a currency format.
• Maintainability: categories and budgets are edited in one place (Categories sheet).
6. Assumptions and limitations
• Assumption: one workbook is used for one month; the Dashboard totals all rows, it does not filter by the Month column.
• Capacity: totals read Transactions rows 4 to 50 only (47 transactions).
• Categories: the Dashboard and chart cover the five categories in Categories rows 4 to 8; the Category list also accepts rows 9 to 11,
but those are not summarised.
• Warning scope: the status compares total expenses with the overall budget; a single overspent category is shown only as a negative
Remaining value.
• Data entry: the drop-down lists do not reject other text, and the sheets are not protected, so formulas can be overwritten.
• Totals use columns: amounts count according to the Income or Expense column, not the Type text. Amounts display in euros (€).
