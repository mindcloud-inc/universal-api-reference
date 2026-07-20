# BILL Spend & Expense: Native API Reference

A consolidated summary of BILL Spend & Expense's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://developer.bill.com/docs/spend-expense-api
- **API base URL:** `https://gateway.{environment}.bill.com/connect/v3`

## Authentication

### Spend & Expense API token

Authenticate with a BILL Spend & Expense API token sent in the apiToken request header.

### Credentials

- **Spend & Expense API token:** `apiKey` · required
- **Environment:** `environment` · required · Environment subdomain for BILL Spend & Expense. Use `prod` for Production or `stage` for Sandbox. MindCloud builds `https://gateway.<environment>.bill.com/connect/v3` automatically from this value.

Send these headers with each API request:

```http
apiToken: <apiKey>
```

[Official authentication documentation](https://developer.bill.com/docs/authentication-with-api-token)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Reimbursement Receipt](actions/add-reimbursement-receipt.md) | `POST spend/reimbursements/:reimbursementId/receipts` | [docs](https://developer.bill.com/reference/addreimbursementreceipt) |
| [Create Budget](actions/create-budget.md) | `POST spend/budgets` | [docs](https://developer.bill.com/reference/createbudget) |
| [Create Reimbursement](actions/create-reimbursement.md) | `POST spend/reimbursements` | [docs](https://developer.bill.com/reference/createreimbursement) |
| [Create Reimbursement Upload URL](actions/create-reimbursement-upload-url.md) | `POST spend/reimbursements/image-upload-url` | [docs](https://developer.bill.com/reference/createimageuploadurl) |
| [Create User](actions/create-user.md) | `POST spend/users` | [docs](https://developer.bill.com/reference/createuser) |
| [Create Vendor Card](actions/create-vendor-card.md) | `POST spend/cards` | [docs](https://developer.bill.com/reference/createbudgetcard) |
| [Delete Budget Member](actions/delete-budget-member.md) | `DELETE spend/budgets/:budgetId/members/:userId` | [docs](https://developer.bill.com/reference/deletebudgetmember) |
| [Get Budget](actions/get-budget.md) | `GET spend/budgets/:budgetId` | [docs](https://developer.bill.com/reference/getbudget) |
| [Get Card](actions/get-card.md) | `GET spend/cards/:cardId` | [docs](https://developer.bill.com/reference/getcard) |
| [Get Reimbursement](actions/get-reimbursement.md) | `GET spend/reimbursements/:reimbursementId` | [docs](https://developer.bill.com/reference/getreimbursement) |
| [Get Transaction](actions/get-transaction.md) | `GET spend/transactions/:transactionId` | [docs](https://developer.bill.com/reference/gettransaction) |
| [Get User](actions/get-user.md) | `GET spend/users/:userId` | [docs](https://developer.bill.com/reference/getuser) |
| [List Budget Members](actions/list-budget-members.md) | `GET spend/budgets/:budgetId/members` | [docs](https://developer.bill.com/reference/listbudgetmembers) |
| [List Budgets](actions/list-budgets.md) | `GET spend/budgets` | [docs](https://developer.bill.com/reference/listbudgets) |
| [List Cards](actions/list-cards.md) | `GET spend/cards` | [docs](https://developer.bill.com/reference/listcards) |
| [List Reimbursements](actions/list-reimbursements.md) | `GET spend/reimbursements` | [docs](https://developer.bill.com/reference/listreimbursements) |
| [List Transactions](actions/list-transactions.md) | `GET spend/transactions` | [docs](https://developer.bill.com/reference/listtransactions) |
| [List Users](actions/list-users.md) | `GET spend/users` | [docs](https://developer.bill.com/reference/listusers) |
| [Update Budget](actions/update-budget.md) | `PATCH spend/budgets/:budgetId` | [docs](https://developer.bill.com/reference/updatebudget) |
| [Update User](actions/update-user.md) | `PATCH spend/users/:userId` | [docs](https://developer.bill.com/reference/updateuser) |
| [Add or Update Budget Member](actions/upsert-budget-member.md) | `PUT spend/budgets/:budgetId/members/:userId` | [docs](https://developer.bill.com/reference/upsertbudgetmember) |
