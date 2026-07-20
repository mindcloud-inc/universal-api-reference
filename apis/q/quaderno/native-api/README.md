# Quaderno: Native API Reference

A consolidated summary of Quaderno's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://developers.quaderno.io/api/
- **OpenAPI specification:** https://developers.quaderno.io/redocusaurus/openapi.yaml
- **API base URL:** `https://sandbox-quadernoapp.com/api`

## Authentication

### OAuth2

Connect a Quaderno Standard account via OAuth2 so MindCloud can act on the seller's behalf.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://sandbox-quadernoapp.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://sandbox-quadernoapp.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `read_write`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://sandbox-quadernoapp.com/oauth/token.

[Official authentication documentation](https://developers.quaderno.io/guides/connect/standard-accounts/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100).

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developers.quaderno.io/api/#tag/Contacts/operation/createContact) |
| [Create Credit Note](actions/create-credit-note.md) | `POST /credits` | [docs](https://developers.quaderno.io/api/#tag/Credits/operation/createCredit) |
| [Create Invoice](actions/create-invoice.md) | `POST /invoices` | [docs](https://developers.quaderno.io/api/#tag/Invoices/operation/createInvoice) |
| [Create Product](actions/create-product.md) | `POST /items` | [docs](https://developers.quaderno.io/api/#tag/Products/operation/createProduct) |
| [Create Receipt](actions/create-receipt.md) | `POST /receipts` | [docs](https://developers.quaderno.io/api/#tag/Receipts/operation/createReceipt) |
| [Create Recurring Document](actions/create-recurring-document.md) | `POST /recurring` | [docs](https://developers.quaderno.io/api/#tag/Recurring-Documents/operation/createRecurring) |
| [Create Tax ID](actions/create-tax-id.md) | `POST /tax_ids` | [docs](https://developers.quaderno.io/api/#tag/Registered-Jurisdictions/operation/createTaxID) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:id` | [docs](https://developers.quaderno.io/api/#tag/Contacts/operation/deleteContact) |
| [Delete Product](actions/delete-product.md) | `DELETE /items/:id` | [docs](https://developers.quaderno.io/api/#tag/Products/operation/deleteProduct) |
| [Deliver Invoice](actions/deliver-invoice.md) | `GET /invoices/:id/deliver` | [docs](https://developers.quaderno.io/api/#tag/Invoices/operation/deliverInvoice) |
| [Deliver Receipt](actions/deliver-receipt.md) | `GET /receipts/:id/deliver` | [docs](https://developers.quaderno.io/api/#tag/Receipts/operation/deliverReceipt) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developers.quaderno.io/api/#tag/Contacts/operation/listContacts) |
| [List Credit Notes](actions/list-credit-notes.md) | `GET /credits` | [docs](https://developers.quaderno.io/api/#tag/Credits/operation/listCredits) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://developers.quaderno.io/api/#tag/Invoices/operation/listInvoices) |
| [List Products](actions/list-products.md) | `GET /items` | [docs](https://developers.quaderno.io/api/#tag/Products/operation/listProducts) |
| [List Receipts](actions/list-receipts.md) | `GET /receipts` | [docs](https://developers.quaderno.io/api/#tag/Receipts/operation/listReceipts) |
| [List Recurring Documents](actions/list-recurring-documents.md) | `GET /recurring` | [docs](https://developers.quaderno.io/api/#tag/Recurring-Documents/operation/listRecurrings) |
| [List Tax Codes](actions/list-tax-codes.md) | `GET /tax_codes` | [docs](https://developers.quaderno.io/api/#tag/Tax-Codes/operation/listTaxCodes) |
| [List Tax IDs](actions/list-tax-ids.md) | `GET /tax_ids` | [docs](https://developers.quaderno.io/api/#tag/Registered-Jurisdictions/operation/listTaxIDs) |
| [Mark Invoice Uncollectible](actions/mark-invoice-uncollectible.md) | `PUT /invoices/:id/mark_uncollectible` | [docs](https://developers.quaderno.io/api/#tag/Invoices/operation/markInvoiceUncollectible) |
| [Record Invoice Payment](actions/record-invoice-payment.md) | `POST /invoices/:id/payments` | [docs](https://developers.quaderno.io/api/#tag/Invoices/operation/recordInvoicePayment) |
| [Retrieve Contact](actions/retrieve-contact.md) | `GET /contacts/:id` | [docs](https://developers.quaderno.io/api/#tag/Contacts/operation/retrieveContact) |
| [Retrieve Invoice](actions/retrieve-invoice.md) | `GET /invoices/:id` | [docs](https://developers.quaderno.io/api/#tag/Invoices/operation/retrieveInvoice) |
| [Retrieve Product](actions/retrieve-product.md) | `GET /items/:id` | [docs](https://developers.quaderno.io/api/#tag/Products/operation/retrieveProduct) |
| [Retrieve Receipt](actions/retrieve-receipt.md) | `GET /receipts/:id` | [docs](https://developers.quaderno.io/api/#tag/Receipts/operation/retrieveReceipt) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:id` | [docs](https://developers.quaderno.io/api/#tag/Contacts/operation/updateContact) |
| [Update Invoice](actions/update-invoice.md) | `PUT /invoices/:id` | [docs](https://developers.quaderno.io/api/#tag/Invoices/operation/updateInvoice) |
| [Update Product](actions/update-product.md) | `PUT /items/:id` | [docs](https://developers.quaderno.io/api/#tag/Products/operation/updateProduct) |
| [Validate Tax ID](actions/validate-tax-id.md) | `GET /tax_ids/validate` | [docs](https://developers.quaderno.io/api/#tag/Tax-IDs/operation/validateTaxID) |
