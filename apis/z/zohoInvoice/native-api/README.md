# Zoho Invoice: Native API Reference

A consolidated summary of Zoho Invoice's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/invoice/api/v3/introduction/
- **OpenAPI specification:** https://www.zoho.com/invoice/api/v3/openapi-all.zip
- **API base URL:** `https://www.zohoapis.com/invoice/v3`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.zoho.com/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoInvoice.fullaccess.all`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.zoho.com/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/invoice/api/v3/oauth/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `per_page` in the query string to set the page size (default 200). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_column` in the query string. Only one sort field is accepted.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://www.zoho.com/invoice/api/v3/contacts/#create-a-contact) |
| [Create Estimate](actions/create-estimate.md) | `POST /estimates` | [docs](https://www.zoho.com/invoice/api/v3/estimates/#create-an-estimate) |
| [Create Expense](actions/create-expense.md) | `POST /expenses` | [docs](https://www.zoho.com/invoice/api/v3/expenses/#create-an-expense) |
| [Create Invoice](actions/create-invoice.md) | `POST /invoices` | [docs](https://www.zoho.com/invoice/api/v3/invoices/#create-an-invoice) |
| [Create Item](actions/create-item.md) | `POST /items` | [docs](https://www.zoho.com/invoice/api/v3/items/#create-an-item) |
| [Create Payment](actions/create-payment.md) | `POST /customerpayments` | [docs](https://www.zoho.com/invoice/api/v3/customer-payments/#create-a-payment) |
| [Email Invoice](actions/email-invoice.md) | `POST /invoices/:invoice_id/email` | [docs](https://www.zoho.com/invoice/api/v3/invoices/#email-an-invoice) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contact_id` | [docs](https://www.zoho.com/invoice/api/v3/contacts/#get-a-contact) |
| [Get Estimate](actions/get-estimate.md) | `GET /estimates/:estimate_id` | [docs](https://www.zoho.com/invoice/api/v3/estimates/#get-an-estimate) |
| [Get Expense](actions/get-expense.md) | `GET /expenses/:expense_id` | [docs](https://www.zoho.com/invoice/api/v3/expenses/#get-an-expense) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/:invoice_id` | [docs](https://www.zoho.com/invoice/api/v3/invoices/#get-an-invoice) |
| [Get Item](actions/get-item.md) | `GET /items/:item_id` | [docs](https://www.zoho.com/invoice/api/v3/items/#retrieve-an-item) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://www.zoho.com/invoice/api/v3/contacts/#list-contacts) |
| [List Customer Payments](actions/list-customer-payments.md) | `GET /customerpayments` | [docs](https://www.zoho.com/invoice/api/v3/customer-payments/#list-customer-payments) |
| [List Estimates](actions/list-estimates.md) | `GET /estimates` | [docs](https://www.zoho.com/invoice/api/v3/estimates/#list-estimates) |
| [List Expenses](actions/list-expenses.md) | `GET /expenses` | [docs](https://www.zoho.com/invoice/api/v3/expenses/#list-expenses) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://www.zoho.com/invoice/api/v3/invoices/#list-invoices) |
| [List Items](actions/list-items.md) | `GET /items` | [docs](https://www.zoho.com/invoice/api/v3/items/#list-items) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://www.zoho.com/invoice/api/v3/organizations/#list-organizations) |
| [Retrieve Payment](actions/retrieve-payment.md) | `GET /customerpayments/:payment_id` | [docs](https://www.zoho.com/invoice/api/v3/customer-payments/#retrieve-a-payment) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:contact_id` | [docs](https://www.zoho.com/invoice/api/v3/contacts/#update-a-contact) |
| [Update Estimate](actions/update-estimate.md) | `PUT /estimates/:estimate_id` | [docs](https://www.zoho.com/invoice/api/v3/estimates/#update-an-estimate) |
| [Update Expense](actions/update-expense.md) | `PUT /expenses/:expense_id` | [docs](https://www.zoho.com/invoice/api/v3/expenses/#update-an-expense) |
| [Update Invoice](actions/update-invoice.md) | `PUT /invoices/:invoice_id` | [docs](https://www.zoho.com/invoice/api/v3/invoices/#update-an-invoice) |
| [Update Item](actions/update-item.md) | `PUT /items/:item_id` | [docs](https://www.zoho.com/invoice/api/v3/items/#update-an-item) |
