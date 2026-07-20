# Bexio: Native API Reference

A consolidated summary of Bexio's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://docs.bexio.com/
- **API base URL:** `https://api.bexio.com`

## Authentication

### OAuth 2.0

Connect Bexio with OAuth 2.0 Authorization Code flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://auth.bexio.com/realms/bexio/protocol/openid-connect/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://auth.bexio.com/realms/bexio/protocol/openid-connect/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `openid offline_access profile company_profile email contact_show contact_edit kb_offer_show kb_offer_edit kb_order_show kb_order_edit kb_delivery_edit kb_invoice_show kb_invoice_edit kb_article_order_show kb_article_order_edit`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://auth.bexio.com/realms/bexio/protocol/openid-connect/token.

[Official authentication documentation](https://docs.bexio.com/#section/Authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 500; maximum 2000). Use `offset` in the query string as the record offset.

## Sorting

Set the sort field with `order_by` in the query string. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /2.0/contact` | [docs](https://docs.bexio.com/#tag/Contacts/operation/v2CreateContact) |
| [Create Expense](actions/create-expense.md) | `POST /4.0/expenses` | [docs](https://docs.bexio.com/#tag/Expenses/operation/ApiExpenses_POST) |
| [Create Invoice](actions/create-invoice.md) | `POST /2.0/kb_invoice` | [docs](https://docs.bexio.com/#tag/Invoices/operation/v2CreateInvoice) |
| [Create Invoice Payment](actions/create-invoice-payment.md) | `POST /2.0/kb_invoice/:invoice_id/payment` | [docs](https://docs.bexio.com/#tag/Invoices/operation/v2CreateInvoicePayment) |
| [Create Order](actions/create-order.md) | `POST /2.0/kb_order` | [docs](https://docs.bexio.com/#tag/Orders/operation/v2CreateOrder) |
| [Create Purchase Order](actions/create-purchase-order.md) | `POST /3.0/purchase_orders` | [docs](https://docs.bexio.com/#tag/Purchase-Orders/operation/v3PurchaseOrderCreate) |
| [Create Quote](actions/create-quote.md) | `POST /2.0/kb_offer` | [docs](https://docs.bexio.com/#tag/Quotes/operation/v2CreateQuote) |
| [Get Contact](actions/get-contact.md) | `GET /2.0/contact/:contact_id` | [docs](https://docs.bexio.com/#tag/Contacts/operation/v2ShowContact) |
| [Get Expense](actions/get-expense.md) | `GET /4.0/expenses/:id` | [docs](https://docs.bexio.com/#tag/Expenses/operation/ApiExpenses_GET) |
| [Get Invoice](actions/get-invoice.md) | `GET /2.0/kb_invoice/:invoice_id` | [docs](https://docs.bexio.com/#tag/Invoices/operation/v2ShowInvoice) |
| [Get Order](actions/get-order.md) | `GET /2.0/kb_order/:order_id` | [docs](https://docs.bexio.com/#tag/Orders/operation/v2ShowOrder) |
| [Get Purchase Order](actions/get-purchase-order.md) | `GET /3.0/purchase_orders/:purchase_order_id` | [docs](https://docs.bexio.com/#tag/Purchase-Orders/operation/v3PurchaseOrderShow) |
| [Get Quote](actions/get-quote.md) | `GET /2.0/kb_offer/:quote_id` | [docs](https://docs.bexio.com/#tag/Quotes/operation/v2ShowQuote) |
| [Issue Invoice](actions/issue-invoice.md) | `POST /2.0/kb_invoice/:invoice_id/issue` | [docs](https://docs.bexio.com/#tag/Invoices/operation/v2IssueInvoice) |
| [Issue Quote](actions/issue-quote.md) | `POST /2.0/kb_offer/:quote_id/issue` | [docs](https://docs.bexio.com/#tag/Quotes/operation/v2IssueQuote) |
| [List Bills](actions/list-bills.md) | `GET /4.0/purchase/bills` | [docs](https://docs.bexio.com/#tag/Bills/operation/ApiBillsList_GET) |
| [List Contacts](actions/list-contacts.md) | `GET /2.0/contact` | [docs](https://docs.bexio.com/#tag/Contacts/operation/v2ListContacts) |
| [List Expenses](actions/list-expenses.md) | `GET /4.0/expenses` | [docs](https://docs.bexio.com/#tag/Expenses/operation/ApiExpensesList_GET) |
| [List Invoices](actions/list-invoices.md) | `GET /2.0/kb_invoice` | [docs](https://docs.bexio.com/#tag/Invoices/operation/v2ListInvoices) |
| [List Orders](actions/list-orders.md) | `GET /2.0/kb_order` | [docs](https://docs.bexio.com/#tag/Orders/operation/v2ListOrders) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `GET /3.0/purchase_orders` | [docs](https://docs.bexio.com/#tag/Purchase-Orders/operation/v3PurchaseOrderList) |
| [List Quotes](actions/list-quotes.md) | `GET /2.0/kb_offer` | [docs](https://docs.bexio.com/#tag/Quotes/operation/v2ListQuotes) |
| [Search Contacts](actions/search-contacts.md) | `POST /2.0/contact/search` | [docs](https://docs.bexio.com/#tag/Contacts/operation/v2SearchContact) |
| [Send Invoice](actions/send-invoice.md) | `POST /2.0/kb_invoice/:invoice_id/send` | [docs](https://docs.bexio.com/#tag/Invoices/operation/v2SendInvoice) |
| [Update Contact](actions/update-contact.md) | `POST /2.0/contact/:contact_id` | [docs](https://docs.bexio.com/#tag/Contacts/operation/v2EditContact) |
