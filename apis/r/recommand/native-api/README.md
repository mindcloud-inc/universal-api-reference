# Recommand: Native API Reference

A consolidated summary of Recommand's API configuration and 57 documented operations, with links to official documentation.

- **Official docs:** https://recommand.eu/en/api-reference
- **OpenAPI specification:** https://recommand.eu/openapi.json
- **API base URL:** `https://app.recommand.eu`

## Authentication

### Basic Auth

Authenticate with a Recommand API key id and secret using standard HTTP Basic authentication.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://recommand.eu/en/docs/authentication)

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (57 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Label to Document](actions/assign-label-to-document.md) | `POST /api/v1/documents/:documentId/labels/:labelId` | [docs](https://recommand.eu/en/reference/documents/assign-label-to-document) |
| [Assign Label to Supplier](actions/assign-label-to-supplier.md) | `POST /api/v1/suppliers/:supplierId/labels/:labelId` | [docs](https://recommand.eu/en/reference/suppliers/assign-label-to-supplier) |
| [Create Company](actions/create-company.md) | `POST /api/v1/companies` | [docs](https://recommand.eu/en/reference/companies/create-company) |
| [Create Company Document Type](actions/create-company-document-type.md) | `POST /api/v1/companies/:companyId/document-types` | [docs](https://recommand.eu/en/reference/company-document-types/create-company-document-type) |
| [Create Company Identifier](actions/create-company-identifier.md) | `POST /api/v1/companies/:companyId/identifiers` | [docs](https://recommand.eu/en/reference/company-identifiers/create-company-identifier) |
| [Create Company Notification Email Address](actions/create-company-notification-email-address.md) | `POST /api/v1/companies/:companyId/notification-email-addresses` | [docs](https://recommand.eu/en/reference/company-notification-email-addresses/create-company-notification-email-address) |
| [Create Label](actions/create-label.md) | `POST /api/v1/labels` | [docs](https://recommand.eu/en/reference/labels/create-label) |
| [Create Playground](actions/create-playground.md) | `POST /api/v1/playgrounds` | [docs](https://recommand.eu/en/reference/playgrounds/create-playground) |
| [Create Webhook](actions/create-webhook.md) | `POST /api/v1/webhooks` | [docs](https://recommand.eu/en/reference/webhooks/create-webhook) |
| [Delete Company](actions/delete-company.md) | `DELETE /api/v1/companies/:companyId` | [docs](https://recommand.eu/en/reference/companies/delete-company) |
| [Delete Company Document Type](actions/delete-company-document-type.md) | `DELETE /api/v1/companies/:companyId/document-types/:documentTypeId` | [docs](https://recommand.eu/en/reference/company-document-types/delete-company-document-type) |
| [Delete Company Identifier](actions/delete-company-identifier.md) | `DELETE /api/v1/companies/:companyId/identifiers/:identifierId` | [docs](https://recommand.eu/en/reference/company-identifiers/delete-company-identifier) |
| [Delete Company Notification Email Address](actions/delete-company-notification-email-address.md) | `DELETE /api/v1/companies/:companyId/notification-email-addresses/:notificationEmailAddressId` | [docs](https://recommand.eu/en/reference/company-notification-email-addresses/delete-company-notification-email-address) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /api/v1/customers/:customerId` | [docs](https://recommand.eu/en/reference/customers/delete-customer) |
| [Delete Document](actions/delete-document.md) | `DELETE /api/v1/documents/:documentId` | [docs](https://recommand.eu/en/reference/documents/delete-document) |
| [Delete Label](actions/delete-label.md) | `DELETE /api/v1/labels/:labelId` | [docs](https://recommand.eu/en/reference/labels/delete-label) |
| [Delete Supplier](actions/delete-supplier.md) | `DELETE /api/v1/suppliers/:supplierId` | [docs](https://recommand.eu/en/reference/suppliers/delete-supplier) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /api/v1/webhooks/:webhookId` | [docs](https://recommand.eu/en/reference/webhooks/delete-webhook) |
| [Download Document Package](actions/download-document-package.md) | `GET /api/v1/documents/:documentId/download-package` | [docs](https://recommand.eu/en/reference/documents/download-document-package) |
| [Get Company](actions/get-company.md) | `GET /api/v1/companies/:companyId` | [docs](https://recommand.eu/en/reference/companies/get-company) |
| [Get Company Document Type](actions/get-company-document-type.md) | `GET /api/v1/companies/:companyId/document-types/:documentTypeId` | [docs](https://recommand.eu/en/reference/company-document-types/get-company-document-type) |
| [Get Company Identifier](actions/get-company-identifier.md) | `GET /api/v1/companies/:companyId/identifiers/:identifierId` | [docs](https://recommand.eu/en/reference/company-identifiers/get-company-identifier) |
| [Get Company Notification Email Address](actions/get-company-notification-email-address.md) | `GET /api/v1/companies/:companyId/notification-email-addresses/:notificationEmailAddressId` | [docs](https://recommand.eu/en/reference/company-notification-email-addresses/get-company-notification-email-address) |
| [Get Customer](actions/get-customer.md) | `GET /api/v1/customers/:customerId` | [docs](https://recommand.eu/en/reference/customers/get-customer) |
| [Get Document](actions/get-document.md) | `GET /api/v1/documents/:documentId` | [docs](https://recommand.eu/en/reference/documents/get-document) |
| [Get Label](actions/get-label.md) | `GET /api/v1/labels/:labelId` | [docs](https://recommand.eu/en/reference/labels/get-label) |
| [Get Playground](actions/get-playground.md) | `GET /api/v1/playgrounds/current` | [docs](https://recommand.eu/en/reference/playgrounds/get-playground) |
| [Get Supplier](actions/get-supplier.md) | `GET /api/v1/suppliers/:supplierId` | [docs](https://recommand.eu/en/reference/suppliers/get-supplier) |
| [Get Webhook](actions/get-webhook.md) | `GET /api/v1/webhooks/:webhookId` | [docs](https://recommand.eu/en/reference/webhooks/get-webhook) |
| [Inbox](actions/inbox.md) | `GET /api/v1/inbox` | [docs](https://recommand.eu/en/reference/documents/inbox) |
| [List Companies](actions/list-companies.md) | `GET /api/v1/companies` | [docs](https://recommand.eu/en/reference/companies/list-companies) |
| [List Company Document Types](actions/list-company-document-types.md) | `GET /api/v1/companies/:companyId/document-types` | [docs](https://recommand.eu/en/reference/company-document-types/list-company-document-types) |
| [List Company Identifiers](actions/list-company-identifiers.md) | `GET /api/v1/companies/:companyId/identifiers` | [docs](https://recommand.eu/en/reference/company-identifiers/list-company-identifiers) |
| [List Company Notification Email Addresses](actions/list-company-notification-email-addresses.md) | `GET /api/v1/companies/:companyId/notification-email-addresses` | [docs](https://recommand.eu/en/reference/company-notification-email-addresses/list-company-notification-email-addresses) |
| [List Customers](actions/list-customers.md) | `GET /api/v1/customers` | [docs](https://recommand.eu/en/reference/customers/list-customers) |
| [List Documents](actions/list-documents.md) | `GET /api/v1/documents` | [docs](https://recommand.eu/en/reference/documents/list-documents) |
| [List Labels](actions/list-labels.md) | `GET /api/v1/labels` | [docs](https://recommand.eu/en/reference/labels/list-labels) |
| [List Suppliers](actions/list-suppliers.md) | `GET /api/v1/suppliers` | [docs](https://recommand.eu/en/reference/suppliers/list-suppliers) |
| [List Webhooks](actions/list-webhooks.md) | `GET /api/v1/webhooks` | [docs](https://recommand.eu/en/reference/webhooks/list-webhooks) |
| [Mark Document as Read](actions/mark-document-as-read.md) | `POST /api/v1/documents/:documentId/mark-as-read` | [docs](https://recommand.eu/en/reference/documents/mark-document-as-read) |
| [Render Document Preview](actions/render-document-preview.md) | `GET /api/v1/documents/:documentId/render/:type` | [docs](https://recommand.eu/en/reference/documents/render-document-preview) |
| [Search Directory](actions/search-directory.md) | `POST /api/v1/search-peppol-directory` | [docs](https://recommand.eu/en/reference/recipients/search-directory) |
| [Send Document](actions/send-document.md) | `POST /api/v1/:companyId/send` | [docs](https://recommand.eu/en/reference/sending/send-document) |
| [Unassign Label from Document](actions/unassign-label-from-document.md) | `DELETE /api/v1/documents/:documentId/labels/:labelId` | [docs](https://recommand.eu/en/reference/documents/unassign-label-from-document) |
| [Unassign Label from Supplier](actions/unassign-label-from-supplier.md) | `DELETE /api/v1/suppliers/:supplierId/labels/:labelId` | [docs](https://recommand.eu/en/reference/suppliers/unassign-label-from-supplier) |
| [Update Company](actions/update-company.md) | `PUT /api/v1/companies/:companyId` | [docs](https://recommand.eu/en/reference/companies/update-company) |
| [Update Company Document Type](actions/update-company-document-type.md) | `PUT /api/v1/companies/:companyId/document-types/:documentTypeId` | [docs](https://recommand.eu/en/reference/company-document-types/update-company-document-type) |
| [Update Company Identifier](actions/update-company-identifier.md) | `PUT /api/v1/companies/:companyId/identifiers/:identifierId` | [docs](https://recommand.eu/en/reference/company-identifiers/update-company-identifier) |
| [Update Company Notification Email Address](actions/update-company-notification-email-address.md) | `PUT /api/v1/companies/:companyId/notification-email-addresses/:notificationEmailAddressId` | [docs](https://recommand.eu/en/reference/company-notification-email-addresses/update-company-notification-email-address) |
| [Update Label](actions/update-label.md) | `PUT /api/v1/labels/:labelId` | [docs](https://recommand.eu/en/reference/labels/update-label) |
| [Update Webhook](actions/update-webhook.md) | `PUT /api/v1/webhooks/:webhookId` | [docs](https://recommand.eu/en/reference/webhooks/update-webhook) |
| [Upsert Customer](actions/upsert-customer.md) | `POST /api/v1/customers` | [docs](https://recommand.eu/en/reference/customers/upsert-customer) |
| [Upsert Supplier](actions/upsert-supplier.md) | `POST /api/v1/suppliers` | [docs](https://recommand.eu/en/reference/suppliers/upsert-supplier) |
| [Verify Authentication](actions/verify-authentication.md) | `GET /api/core/auth/verify` | [docs](https://recommand.eu/en/reference/authentication/verify-authentication) |
| [Verify Company](actions/verify-company.md) | `POST /api/v1/companies/:companyId/verify` | [docs](https://recommand.eu/en/reference/companies/verify-company) |
| [Verify Document Support](actions/verify-document-support.md) | `POST /api/v1/verify-document-support` | [docs](https://recommand.eu/en/reference/recipients/verify-document-support) |
| [Verify Recipient](actions/verify-recipient.md) | `POST /api/v1/verify` | [docs](https://recommand.eu/en/reference/recipients/verify-recipient) |
