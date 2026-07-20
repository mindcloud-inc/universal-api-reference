# <img src="https://images.mindcloud.co/apps/icons/b-illspend-expense_1782829833332.png" alt="BILL Spend & Expense logo" width="28" height="28"> BILL Spend & Expense: Universal API

Manage BILL Spend & Expense budgets, users, cards, transactions, and reimbursements.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bILLSpendExpense/latest
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bill.com/
- **Vendor API docs:** https://developer.bill.com/docs/spend-expense-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Transactions](actions/list-transactions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bILLSpendExpense/latest/actions/list-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Budget

| Action | Method | Description |
| --- | --- | --- |
| [Create Budget](actions/create-budget.md) | POST | Creates a new budget in BILL Spend & Expense. |
| [Get Budget](actions/get-budget.md) | GET | Retrieves a budget from BILL Spend & Expense. |
| [List Budgets](actions/list-budgets.md) | GET | Retrieves budgets from BILL Spend & Expense. |
| [Update Budget](actions/update-budget.md) | PUT | Updates an existing budget in BILL Spend & Expense. |

### Budgets

| Action | Method | Description |
| --- | --- | --- |
| [Delete Budget Member](actions/delete-budget-member.md) | DELETE | Deletes an existing budget member from BILL Spend & Expense. |
| [List Budget Members](actions/list-budget-members.md) | GET | Retrieves members for a budget in BILL Spend & Expense. |
| [Add or Update Budget Member](actions/upsert-budget-member.md) | PUT | Adds or updates a budget member in BILL Spend & Expense. |

### Card

| Action | Method | Description |
| --- | --- | --- |
| [Get Card](actions/get-card.md) | GET | Retrieves a vendor card from BILL Spend & Expense. |
| [List Cards](actions/list-cards.md) | GET | Retrieves vendor cards from BILL Spend & Expense. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Reimbursement Upload URL](actions/create-reimbursement-upload-url.md) | POST | Creates a reimbursement upload URL in BILL Spend & Expense. |
| [Create Vendor Card](actions/create-vendor-card.md) | POST | Creates a new vendor card in BILL Spend & Expense. |

### Reimbursement

| Action | Method | Description |
| --- | --- | --- |
| [Create Reimbursement](actions/create-reimbursement.md) | POST | Creates a new reimbursement in BILL Spend & Expense. |
| [Get Reimbursement](actions/get-reimbursement.md) | GET | Retrieves a reimbursement from BILL Spend & Expense. |
| [List Reimbursements](actions/list-reimbursements.md) | GET | Retrieves reimbursements from BILL Spend & Expense. |

### Reimbursements

| Action | Method | Description |
| --- | --- | --- |
| [Add Reimbursement Receipt](actions/add-reimbursement-receipt.md) | POST | Adds a receipt to a reimbursement in BILL Spend & Expense. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves a transaction from BILL Spend & Expense. |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves transactions from BILL Spend & Expense. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in BILL Spend & Expense. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from BILL Spend & Expense. |
| [List Users](actions/list-users.md) | GET | Retrieves users from BILL Spend & Expense. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in BILL Spend & Expense. |

