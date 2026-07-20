# MoneyBird: Native API Reference

A consolidated summary of MoneyBird's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://developer.moneybird.com/api
- **API base URL:** `https://moneybird.com/api/v2`

## Authentication

### OAuth2

OAuth 2.0 authorization code flow for MoneyBird.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://moneybird.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://moneybird.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `sales_invoices documents estimates settings`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://moneybird.com/oauth/token.

[Official authentication documentation](https://developer.moneybird.com/authentication)

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /:administrationId/contacts.json` | [docs](https://developer.moneybird.com/api/contacts) |
| [Create Estimate](actions/create-estimate.md) | `POST /:administrationId/estimates.json` | [docs](https://developer.moneybird.com/api/estimates/) |
| [Create General Document](actions/create-general-document.md) | `POST /:administrationId/documents/general_documents.json` | [docs](https://developer.moneybird.com/api/documents-general-documents/) |
| [Create Product](actions/create-product.md) | `POST /:administrationId/products.json` | [docs](https://developer.moneybird.com/api/products) |
| [Create Sales Invoice](actions/create-sales-invoice.md) | `POST /:administrationId/sales_invoices.json` | [docs](https://developer.moneybird.com/api/sales-invoices/) |
| [Create Subscription](actions/create-subscription.md) | `POST /:administrationId/subscriptions.json` | [docs](https://developer.moneybird.com/integration/managing-subscriptions) |
| [Create Webhook](actions/create-webhook.md) | `POST /:administrationId/webhooks.json` | [docs](https://developer.moneybird.com/api/webhooks/) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /:administrationId/webhooks/:webhookId.json` | [docs](https://developer.moneybird.com/api/webhooks/) |
| [Get Contact](actions/get-contact.md) | `GET /:administrationId/contacts/:contactId.json` | [docs](https://developer.moneybird.com/api/contacts) |
| [Get Estimate](actions/get-estimate.md) | `GET /:administrationId/estimates/:estimateId.json` | [docs](https://developer.moneybird.com/api/estimates/) |
| [Get General Document](actions/get-general-document.md) | `GET /:administrationId/documents/general_documents/:generalDocumentId.json` | [docs](https://developer.moneybird.com/api/documents-general-documents/) |
| [Get Product](actions/get-product.md) | `GET /:administrationId/products/:productId.json` | [docs](https://developer.moneybird.com/api/products) |
| [Get Sales Invoice](actions/get-sales-invoice.md) | `GET /:administrationId/sales_invoices/:salesInvoiceId.json` | [docs](https://developer.moneybird.com/api/sales-invoices/) |
| [List Administrations](actions/list-administrations.md) | `GET /administrations.json` | [docs](https://developer.moneybird.com/api/administrations/) |
| [List Contacts](actions/list-contacts.md) | `GET /:administrationId/contacts.json` | [docs](https://developer.moneybird.com/api/contacts) |
| [List Estimates](actions/list-estimates.md) | `GET /:administrationId/estimates.json` | [docs](https://developer.moneybird.com/api/estimates/) |
| [List General Documents](actions/list-general-documents.md) | `GET /:administrationId/documents/general_documents.json` | [docs](https://developer.moneybird.com/api/documents-general-documents/) |
| [List Products](actions/list-products.md) | `GET /:administrationId/products.json` | [docs](https://developer.moneybird.com/api/products) |
| [List Sales Invoices](actions/list-sales-invoices.md) | `GET /:administrationId/sales_invoices.json` | [docs](https://developer.moneybird.com/api/sales-invoices/) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /:administrationId/subscriptions.json` | [docs](https://developer.moneybird.com/integration/managing-subscriptions) |
| [List Webhooks](actions/list-webhooks.md) | `GET /:administrationId/webhooks.json` | [docs](https://developer.moneybird.com/api/webhooks/) |
| [Send Estimate](actions/send-estimate.md) | `PATCH /:administrationId/estimates/:estimateId/send_estimate.json` | [docs](https://developer.moneybird.com/api/estimates/) |
| [Send Sales Invoice](actions/send-sales-invoice.md) | `PATCH /:administrationId/sales_invoices/:salesInvoiceId/send_invoice.json` | [docs](https://developer.moneybird.com/api/sales-invoices/) |
| [Update Contact](actions/update-contact.md) | `PATCH /:administrationId/contacts/:contactId.json` | [docs](https://developer.moneybird.com/api/contacts) |
| [Update Estimate](actions/update-estimate.md) | `PATCH /:administrationId/estimates/:estimateId.json` | [docs](https://developer.moneybird.com/api/estimates/) |
| [Update Product](actions/update-product.md) | `PATCH /:administrationId/products/:productId.json` | [docs](https://developer.moneybird.com/api/products) |
| [Update Sales Invoice](actions/update-sales-invoice.md) | `PATCH /:administrationId/sales_invoices/:salesInvoiceId.json` | [docs](https://developer.moneybird.com/api/sales-invoices/) |
