# Zoho Books: Native API Reference

A consolidated summary of Zoho Books's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/books/api/v3/introduction/
- **API base URL:** `https://www.zohoapis.com/books/v3`

## Authentication

### OAuth 2.0

### Credentials

- **Zoho Domain:** `zohoDomain` · required · Zoho Books data center suffix from your app URL. Use com, eu, in, com.au, jp, ca, com.cn, or sa.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.zoho.com/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoBooks.contacts.ALL,ZohoBooks.settings.ALL,ZohoBooks.estimates.ALL,ZohoBooks.invoices.ALL,ZohoBooks.customerpayments.ALL,ZohoBooks.creditnotes.ALL,ZohoBooks.projects.ALL,ZohoBooks.expenses.ALL,ZohoBooks.salesorders.ALL,ZohoBooks.purchaseorders.ALL,ZohoBooks.bills.ALL,ZohoBooks.debitnotes.ALL,ZohoBooks.vendorpayments.ALL,ZohoBooks.banking.ALL,ZohoBooks.accountants.ALL`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.zoho.com/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/books/api/v3/oauth/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `organizations`.

## Pagination

Use `per_page` in the query string to set the page size (default 200). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_column` in the query string. Only one sort field is accepted.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bill](actions/create-bill.md) | `POST /bills` | [docs](https://www.zoho.com/books/api/v3/bills/#create-a-bill) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://www.zoho.com/books/api/v3/contacts/#create-a-contact) |
| [Create Customer Payment](actions/create-customer-payment.md) | `POST /customerpayments` | [docs](https://www.zoho.com/books/api/v3/customer-payments/#create-a-payment) |
| [Create Estimate](actions/create-estimate.md) | `POST /estimates` | [docs](https://www.zoho.com/books/api/v3/estimates/#create-an-estimate) |
| [Create Invoice](actions/create-invoice.md) | `POST /invoices` | [docs](https://www.zoho.com/books/api/v3/invoices/#create-an-invoice) |
| [Create Item](actions/create-item.md) | `POST /items` | [docs](https://www.zoho.com/books/api/v3/items/#create-an-item) |
| [Get Bill](actions/get-bill.md) | `GET /bills/:bill_id` | [docs](https://www.zoho.com/books/api/v3/bills/#get-a-bill) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contact_id` | [docs](https://www.zoho.com/books/api/v3/contacts/#get-contact) |
| [Get Estimate](actions/get-estimate.md) | `GET /estimates/:estimate_id` | [docs](https://www.zoho.com/books/api/v3/estimates/#get-an-estimate) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/:invoice_id` | [docs](https://www.zoho.com/books/api/v3/invoices/#get-an-invoice) |
| [Get Item](actions/get-item.md) | `GET /items/:item_id` | [docs](https://www.zoho.com/books/api/v3/items/#get-an-item) |
| [List Bills](actions/list-bills.md) | `GET /bills` | [docs](https://www.zoho.com/books/api/v3/bills/#list-bills) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://www.zoho.com/books/api/v3/contacts/#list-contacts) |
| [List Customer Payments](actions/list-customer-payments.md) | `GET /customerpayments` | [docs](https://www.zoho.com/books/api/v3/customer-payments/#list-customer-payments) |
| [List Estimates](actions/list-estimates.md) | `GET /estimates` | [docs](https://www.zoho.com/books/api/v3/estimates/#list-estimates) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://www.zoho.com/books/api/v3/invoices/#list-invoices) |
| [List Items](actions/list-items.md) | `GET /items` | [docs](https://www.zoho.com/books/api/v3/items/#list-items) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://www.zoho.com/books/api/v3/introduction/#organizations) |
| [Retrieve Customer Payment](actions/retrieve-customer-payment.md) | `GET /customerpayments/:payment_id` | [docs](https://www.zoho.com/books/api/v3/customer-payments/#retrieve-a-payment) |
| [Update Bill](actions/update-bill.md) | `PUT /bills/:bill_id` | [docs](https://www.zoho.com/books/api/v3/bills/#update-a-bill) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:contact_id` | [docs](https://www.zoho.com/books/api/v3/contacts/#update-a-contact) |
| [Update Customer Payment](actions/update-customer-payment.md) | `PUT /customerpayments/:payment_id` | [docs](https://www.zoho.com/books/api/v3/customer-payments/#update-a-payment) |
| [Update Estimate](actions/update-estimate.md) | `PUT /estimates/:estimate_id` | [docs](https://www.zoho.com/books/api/v3/estimates/#update-an-estimate) |
| [Update Invoice](actions/update-invoice.md) | `PUT /invoices/:invoice_id` | [docs](https://www.zoho.com/books/api/v3/invoices/#update-an-invoice) |
| [Update Item](actions/update-item.md) | `PUT /items/:item_id` | [docs](https://www.zoho.com/books/api/v3/items/#update-an-item) |
