# InvoiceBerry: Native API Reference

A consolidated summary of InvoiceBerry's API configuration and 45 documented operations, with links to official documentation.

- **Official docs:** https://www.invoiceberry.com/api-documentation/
- **API base URL:** `https://www.invoiceberry.com`

## Authentication

### API Key

Connect with your InvoiceBerry API key and API password from API Preferences.

### Credentials

- **API Key:** `apiKey` · required
- **API Password:** `apiPassword` · required · InvoiceBerry API password from API Preferences.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.invoiceberry.com/en/article/5-how-to-connect-invoiceberry-to-hundreds-of-other-apps-with-zapier)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Endpoints (45 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Expense](actions/create-expense.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#new-expense) |
| [Create Expense Category](actions/create-expense-category.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#new-category) |
| [Create Expense Vendor](actions/create-expense-vendor.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#new-vendors) |
| [Create Item](actions/create-item.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#new-item) |
| [Create Tax](actions/create-tax.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#new-tax) |
| [Get Client](actions/get-client.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-client) |
| [Get Client Credit History](actions/get-client-credit-history.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#client-credit-history) |
| [Get Credit Note](actions/get-credit-note.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-credit-note) |
| [Get Expense](actions/get-expense.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-expense) |
| [Get Invoice](actions/get-invoice.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-invoice) |
| [Get Item](actions/get-item.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-item) |
| [Get Quote](actions/get-quote.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-quote) |
| [Get Recurring Invoice](actions/get-recurring-invoice.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-invoice-2) |
| [Get Total Clients](actions/get-total-clients.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-total-clients) |
| [Get Total Credit Notes](actions/get-total-credit-notes.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-total-credit-notes) |
| [Get Total Expenses](actions/get-total-expenses.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-total-expense) |
| [Get Total Invoices](actions/get-total-invoices.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-total-invoices) |
| [Get Total Items](actions/get-total-items.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-total-items) |
| [Get Total Quotes](actions/get-total-quotes.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-total-quotes) |
| [Get Total Recurring Invoices](actions/get-total-recurring-invoices.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-total-invoices-2) |
| [List Client Reports](actions/list-client-reports.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#client-reports) |
| [List Clients](actions/list-clients.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-clients) |
| [List Countries](actions/list-countries.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-countries) |
| [List Credit Note Client Contacts](actions/list-credit-note-client-contacts.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-credit-note-client-contacts) |
| [List Credit Notes](actions/list-credit-notes.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-credit-notes) |
| [List Currencies](actions/list-currencies.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-currencies) |
| [List Expense Categories](actions/list-expense-categories.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-categories) |
| [List Expense Vendors](actions/list-expense-vendors.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-vendors) |
| [List Invoice Client Contacts](actions/list-invoice-client-contacts.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-invoice-client-contacts) |
| [List Invoices](actions/list-invoices.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-invoices) |
| [List Items](actions/list-items.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-items) |
| [List Languages](actions/list-languages.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-languages) |
| [List Payment Methods](actions/list-payment-methods.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-payment-methods) |
| [List Quote Client Contacts](actions/list-quote-client-contacts.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-quote-client-contacts) |
| [List Quotes](actions/list-quotes.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-quotes) |
| [List Recurring Frequencies](actions/list-recurring-frequencies.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-recurring-frequencies) |
| [List Recurring Invoices](actions/list-recurring-invoices.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-invoices-2) |
| [List Taxes](actions/list-taxes.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#get-taxes) |
| [Update Client](actions/update-client.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#edit-client) |
| [Update Credit Note](actions/update-credit-note.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#edit-credit-note) |
| [Update Expense](actions/update-expense.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#edit-expense) |
| [Update Invoice](actions/update-invoice.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#edit-invoice) |
| [Update Item](actions/update-item.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#edit-item) |
| [Update Quote](actions/update-quote.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#edit-quote) |
| [Update Recurring Invoice](actions/update-recurring-invoice.md) | `POST /api` | [docs](https://www.invoiceberry.com/api-documentation/#edit-invoice-2) |
