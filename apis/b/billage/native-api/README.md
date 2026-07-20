# Billage: Native API Reference

A consolidated summary of Billage's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://app.getbillage.com/api/documentation.html
- **OpenAPI specification:** https://app.getbillage.com/api/v2/api-docs?group=api
- **API base URL:** `https://app.getbillage.com/api`

## Authentication

### API Key

Authenticate with the Billage company API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://help.getbillage.com/es/articles/2723596-como-generar-una-api-key-de-billage)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `total_pages`. The current page number is read from `current_page`.

## Pagination

Use `elements` in the query string to set the page size (default 25). Use `start` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Multiple sort fields can be combined.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | `POST /v2/accounts` | [docs](https://app.getbillage.com/api/documentation.html#/Accounts/accountCreate) |
| [Create Budget](actions/create-budget.md) | `POST /v2/budgets` | [docs](https://app.getbillage.com/api/documentation.html#/Budgets/budgetCreate) |
| [Create Contact](actions/create-contact.md) | `POST /v2/contacts` | [docs](https://app.getbillage.com/api/documentation.html#/Contacts/contactCreate) |
| [Create Invoice](actions/create-invoice.md) | `POST /v2/invoices` | [docs](https://app.getbillage.com/api/documentation.html#/Invoices/invoiceCreate) |
| [Create Product](actions/create-product.md) | `POST /v2/products` | [docs](https://app.getbillage.com/api/documentation.html#/Products/productCreate) |
| [Create Spending](actions/create-spending.md) | `POST /v2/spendings` | [docs](https://app.getbillage.com/api/documentation.html#/Spendings/spendingCreate) |
| [Get Account](actions/get-account.md) | `GET /v2/accounts/:accountId` | [docs](https://app.getbillage.com/api/documentation.html#/Accounts/accountById) |
| [Get Budget](actions/get-budget.md) | `GET /v2/budgets/:id` | [docs](https://app.getbillage.com/api/documentation.html#/Budgets/budgetFindById) |
| [Get Company Info](actions/get-company-info.md) | `GET /v2/companies/info` | [docs](https://app.getbillage.com/api/documentation.html#/Companies/companyInformation) |
| [Get Contact](actions/get-contact.md) | `GET /v2/contacts/:id` | [docs](https://app.getbillage.com/api/documentation.html#/Contacts/contactById) |
| [Get Invoice by Reference](actions/get-invoice-by-reference.md) | `GET /v2/invoices/by-ref` | [docs](https://app.getbillage.com/api/documentation.html#/Invoices/invoicesListByReference) |
| [Get Spending by Reference](actions/get-spending-by-reference.md) | `GET /v2/spendings/by-ref` | [docs](https://app.getbillage.com/api/documentation.html#/Spendings/spendingByRef) |
| [List Accounts](actions/list-accounts.md) | `GET /v2/accounts` | [docs](https://app.getbillage.com/api/documentation.html#/Accounts/accountsByParameters) |
| [List Budgets](actions/list-budgets.md) | `GET /v2/budgets` | [docs](https://app.getbillage.com/api/documentation.html#/Budgets/budgetsByParameters) |
| [List Contacts](actions/list-contacts.md) | `GET /v2/contacts` | [docs](https://app.getbillage.com/api/documentation.html#/Contacts/contactsByParameters) |
| [List Invoices](actions/list-invoices.md) | `GET /v2/invoices` | [docs](https://app.getbillage.com/api/documentation.html#/Invoices/invoicesByParameters) |
| [List Products](actions/list-products.md) | `GET /v2/products` | [docs](https://app.getbillage.com/api/documentation.html#/Products/productsByParameters) |
| [List Spendings](actions/list-spendings.md) | `GET /v2/spendings` | [docs](https://app.getbillage.com/api/documentation.html#/Spendings/spendingsByParameters) |
| [Update Account](actions/update-account.md) | `PUT /v2/accounts` | [docs](https://app.getbillage.com/api/documentation.html#/Accounts/accountUpdate) |
| [Update Budget](actions/update-budget.md) | `PUT /v2/budgets` | [docs](https://app.getbillage.com/api/documentation.html#/Budgets/budgetUpdate) |
| [Update Contact](actions/update-contact.md) | `PUT /v2/contacts` | [docs](https://app.getbillage.com/api/documentation.html#/Contacts/contactUpdate) |
| [Update Invoice](actions/update-invoice.md) | `PUT /v2/invoices` | [docs](https://app.getbillage.com/api/documentation.html#/Invoices/invoiceUpdate) |
| [Update Product](actions/update-product.md) | `PUT /v2/products` | [docs](https://app.getbillage.com/api/documentation.html#/Products/productUpdate) |
| [Update Spending](actions/update-spending.md) | `PUT /v2/spendings` | [docs](https://app.getbillage.com/api/documentation.html#/Spendings/spendingUpdate) |
