# Visma eAccounting: Native API Reference

A consolidated summary of Visma eAccounting's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://eaccountingapi.vismaonline.com/scalar/v2
- **OpenAPI specification:** https://eaccountingapi.vismaonline.com/openapi/v2.json
- **API base URL:** `https://eaccountingapi.vismaonline.com`

## Authentication

### OAuth2

Visma recommends company selection during OAuth. The registered callback URI must exactly match the current MindCloud app slug callback.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://identity.vismaonline.com/connect/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://identity.vismaonline.com/connect/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ea:api offline_access ea:sales`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://identity.vismaonline.com/connect/token.

[Official authentication documentation](https://developer.vismaonline.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `$pagesize` in the query string to set the page size (default 50; accepted range 1–1000). Use `$page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `$orderby` in the query string. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accept Quote](actions/accept-quote.md) | `PUT /quotes/{id}/accept` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#quotes/put/quotes/{id}/accept) |
| [Complete Order](actions/complete-order.md) | `POST /orders/{id}/completed` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#orders/post/orders/{id}/completed) |
| [Convert Customer Invoice Draft To Customer Invoice](actions/convert-customer-invoice-draft-to-customer-invoice.md) | `POST /customerinvoicedrafts/{customerInvoiceDraftId}/convert` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#customerinvoicedrafts/post/customerinvoicedrafts/{customerInvoiceDraftId}/convert) |
| [Convert Order To Customer Invoice](actions/convert-order-to-customer-invoice.md) | `POST /orders/{id}/convert` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#orders/post/orders/{id}/convert) |
| [Convert Quote To Customer Invoice](actions/convert-quote-to-customer-invoice.md) | `POST /quotes/{id}/converttocustomerinvoice` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#quotes/post/quotes/{id}/converttocustomerinvoice) |
| [Convert Quote To Order](actions/convert-quote-to-order.md) | `POST /quotes/{id}/converttoorder` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#quotes/post/quotes/{id}/converttoorder) |
| [Create Article](actions/create-article.md) | `POST /articles` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#articles/post/articles) |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#customers/post/customers) |
| [Create Customer Invoice](actions/create-customer-invoice.md) | `POST /customerinvoices` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#customerinvoices/post/customerinvoices) |
| [Create Customer Invoice Draft](actions/create-customer-invoice-draft.md) | `POST /customerinvoicedrafts` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#customerinvoicedrafts/post/customerinvoicedrafts) |
| [Create Customer Invoice Payment](actions/create-customer-invoice-payment.md) | `POST /customerinvoices/{invoiceId}/payments` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#customerinvoices/post/customerinvoices/{invoiceId}/payments) |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#orders/post/orders) |
| [Create Order Backorder](actions/create-order-backorder.md) | `POST /orders/{id}/backorder` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#orders/post/orders/{id}/backorder) |
| [Create Quote](actions/create-quote.md) | `POST /quotes` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#quotes/post/quotes) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /customers/{customerId}` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#customers/delete/customers/{customerId}) |
| [Delete Customer Invoice Draft](actions/delete-customer-invoice-draft.md) | `DELETE /customerinvoicedrafts/{customerInvoiceDraftId}` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#customerinvoicedrafts/delete/customerinvoicedrafts/{customerInvoiceDraftId}) |
| [Get Article](actions/get-article.md) | `GET /articles/{articleId}` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#articles/get/articles/{articleId}) |
| [Get Customer](actions/get-customer.md) | `GET /customers/{customerId}` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#customers/get/customers/{customerId}) |
| [Get Customer Invoice](actions/get-customer-invoice.md) | `GET /customerinvoices/{invoiceId}` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#customerinvoices/get/customerinvoices/{invoiceId}) |
| [Get Customer Invoice Draft](actions/get-customer-invoice-draft.md) | `GET /customerinvoicedrafts/{invoiceDraftId}` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#customerinvoicedrafts/get/customerinvoicedrafts/{invoiceDraftId}) |
| [Get Customer Invoice PDF](actions/get-customer-invoice-pdf.md) | `GET /customerinvoices/{invoiceId}/pdf` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#customerinvoices/get/customerinvoices/{invoiceId}/pdf) |
| [Get Order](actions/get-order.md) | `GET /orders/{id}` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#orders/get/orders/{id}) |
| [Get Quote](actions/get-quote.md) | `GET /quotes/{id}` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#quotes/get/quotes/{id}) |
| [List Articles](actions/list-articles.md) | `GET /articles` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#articles/get/articles) |
| [List Customer Invoice Drafts](actions/list-customer-invoice-drafts.md) | `GET /customerinvoicedrafts` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#customerinvoicedrafts/get/customerinvoicedrafts) |
| [List Customer Invoices](actions/list-customer-invoices.md) | `GET /customerinvoices` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#customerinvoices/get/customerinvoices) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#customers/get/customers) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#orders/get/orders) |
| [List Quotes](actions/list-quotes.md) | `GET /quotes` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#quotes/get/quotes) |
| [Print Order As PDF](actions/print-order-as-pdf.md) | `GET /orders/{id}/print` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#orders/get/orders/{id}/print) |
| [Replace Article](actions/replace-article.md) | `PUT /articles/{articleId}` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#articles/put/articles/{articleId}) |
| [Replace Customer Invoice Draft](actions/replace-customer-invoice-draft.md) | `PUT /customerinvoicedrafts/{customerInvoiceDraftId}` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#customerinvoicedrafts/put/customerinvoicedrafts/{customerInvoiceDraftId}) |
| [Send Customer Invoice Email](actions/send-customer-invoice-email.md) | `POST /customerinvoices/{invoiceId}/email` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#customerinvoices/post/customerinvoices/{invoiceId}/email) |
| [Send Customer Invoice Payment Reminder](actions/send-customer-invoice-payment-reminder.md) | `POST /customerinvoices/{invoiceId}/paymentreminders` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#customerinvoices/post/customerinvoices/{invoiceId}/paymentreminders) |
| [Send Order Email](actions/send-order-email.md) | `POST /orders/{id}/email` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#orders/post/orders/{id}/email) |
| [Send Quote Email](actions/send-quote-email.md) | `POST /quotes/{id}/email` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#quotes/post/quotes/{id}/email) |
| [Update Customer](actions/update-customer.md) | `PUT /customers/{customerId}` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#customers/put/customers/{customerId}) |
| [Update Order](actions/update-order.md) | `PUT /orders/{id}` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#orders/put/orders/{id}) |
| [Update Quote](actions/update-quote.md) | `PUT /quotes/{id}` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#quotes/put/quotes/{id}) |
| [Void Customer Invoice](actions/void-customer-invoice.md) | `POST /customerinvoices/{invoiceId}/void` | [docs](https://eaccountingapi.vismaonline.com/scalar/v2#customerinvoices/post/customerinvoices/{invoiceId}/void) |
