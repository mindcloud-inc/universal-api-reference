# Finmei: Native API Reference

A consolidated summary of Finmei's API configuration and 17 documented operations.

- **API base URL:** `https://app.finmei.com/api`

## Authentication

### Bearer Token

Use a Finmei API token in the Authorization bearer header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://finmei.com/about)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (17 documented)

| Operation | Method & path |
| --- | --- |
| [Create Expense](actions/create-expense.md) | `POST /expenses` |
| [Create Invoice](actions/create-invoice.md) | `POST /invoices` |
| [Delete Expense](actions/delete-expense.md) | `DELETE /expenses/:expenseId` |
| [Delete Invoice](actions/delete-invoice.md) | `DELETE /invoices/:invoiceId` |
| [Download Expense](actions/download-expense.md) | `GET /expenses/:expenseId/download` |
| [Download Invoice](actions/download-invoice.md) | `GET /invoices/:invoiceId/download` |
| [Get Expense](actions/get-expense.md) | `GET /expenses/:expenseId` |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/:invoiceId` |
| [Get Profile](actions/get-profile.md) | `GET /profile` |
| [List Currencies](actions/list-currencies.md) | `GET /currencies` |
| [List Expenses](actions/list-expenses.md) | `GET /expenses` |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` |
| [Patch Expense](actions/patch-expense.md) | `PATCH /expenses/:expenseId` |
| [Patch Invoice](actions/patch-invoice.md) | `PATCH /invoices/:invoiceId` |
| [Replace Expense File](actions/replace-expense-file.md) | `POST /expenses/:expenseId/file` |
| [Update Expense](actions/update-expense.md) | `PUT /expenses/:expenseId` |
| [Update Invoice](actions/update-invoice.md) | `PUT /invoices/:invoiceId` |
