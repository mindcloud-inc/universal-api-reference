# Lexware Office: Native API Reference

A consolidated summary of Lexware Office's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://developers.lexware.io/docs/
- **API base URL:** `https://api.lexware.io`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.lexware.io/docs/#samples-accessing-endpoints-with-your-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `content`. The total page count is read from `totalPages`. The current page number is read from `number`.

## Pagination

Use `size` in the query string to set the page size (default 25). Use `page` in the query string to choose the page; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Article](actions/create-article.md) | `POST /v1/articles` | [docs](https://developers.lexware.io/docs/#articles-endpoint-create-an-article) |
| [Create Contact](actions/create-contact.md) | `POST /v1/contacts` | [docs](https://developers.lexware.io/docs/#contacts-endpoint-create-a-contact) |
| [Create Credit Note](actions/create-credit-note.md) | `POST /v1/credit-notes` | [docs](https://developers.lexware.io/docs/#credit-notes-endpoint-create-a-credit-note) |
| [Create Invoice](actions/create-invoice.md) | `POST /v1/invoices` | [docs](https://developers.lexware.io/docs/#invoices-endpoint-create-an-invoice) |
| [Create Order Confirmation](actions/create-order-confirmation.md) | `POST /v1/order-confirmations` | [docs](https://developers.lexware.io/docs/#order-confirmations-endpoint-create-an-order-confirmation) |
| [Create Quotation](actions/create-quotation.md) | `POST /v1/quotations` | [docs](https://developers.lexware.io/docs/#quotations-endpoint-create-a-quotation) |
| [Create Voucher](actions/create-voucher.md) | `POST /v1/vouchers` | [docs](https://developers.lexware.io/docs/#vouchers-endpoint-create-a-voucher) |
| [Delete Article](actions/delete-article.md) | `DELETE /v1/articles/:id` | [docs](https://developers.lexware.io/docs/#articles-endpoint-delete-an-article) |
| [Download Credit Note File](actions/download-credit-note-file.md) | `GET /v1/credit-notes/:id/file` | [docs](https://developers.lexware.io/docs/#credit-notes-endpoint-download-a-credit-note-file) |
| [Download File](actions/download-file.md) | `GET /v1/files/:id` | [docs](https://developers.lexware.io/docs/#files-endpoint-download-a-file) |
| [Download Invoice File](actions/download-invoice-file.md) | `GET /v1/invoices/:id/file` | [docs](https://developers.lexware.io/docs/#invoices-endpoint-download-an-invoice-file) |
| [Download Order Confirmation File](actions/download-order-confirmation-file.md) | `GET /v1/order-confirmations/:id/file` | [docs](https://developers.lexware.io/docs/#order-confirmations-endpoint-download-an-order-confirmation-file) |
| [Download Quotation File](actions/download-quotation-file.md) | `GET /v1/quotations/:id/file` | [docs](https://developers.lexware.io/docs/#quotations-endpoint-download-a-quotation-file) |
| [List Articles](actions/list-articles.md) | `GET /v1/articles` | [docs](https://developers.lexware.io/docs/#articles-endpoint-filtering-articles) |
| [List Contacts](actions/list-contacts.md) | `GET /v1/contacts` | [docs](https://developers.lexware.io/docs/#contacts-endpoint-filtering-contacts) |
| [List Voucher Metadata](actions/list-voucher-metadata.md) | `GET /v1/voucherlist` | [docs](https://developers.lexware.io/docs/#voucherlist-endpoint-retrieve-and-filter-voucherlist) |
| [Render Credit Note Document](actions/render-credit-note-document.md) | `GET /v1/credit-notes/:id/document` | [docs](https://developers.lexware.io/docs/#credit-notes-endpoint-render-a-credit-note-document-pdf) |
| [Render Invoice Document](actions/render-invoice-document.md) | `GET /v1/invoices/:id/document` | [docs](https://developers.lexware.io/docs/#invoices-endpoint-render-an-invoice-document-pdf) |
| [Render Order Confirmation Document](actions/render-order-confirmation-document.md) | `GET /v1/order-confirmations/:id/document` | [docs](https://developers.lexware.io/docs/#order-confirmations-endpoint-render-an-order-confirmation-document-pdf) |
| [Render Quotation Document](actions/render-quotation-document.md) | `GET /v1/quotations/:id/document` | [docs](https://developers.lexware.io/docs/#quotations-endpoint-render-a-quotation-document-pdf) |
| [Retrieve Article](actions/retrieve-article.md) | `GET /v1/articles/:id` | [docs](https://developers.lexware.io/docs/#articles-endpoint-retrieve-an-article) |
| [Retrieve Contact](actions/retrieve-contact.md) | `GET /v1/contacts/:id` | [docs](https://developers.lexware.io/docs/#contacts-endpoint-retrieve-a-contact) |
| [Retrieve Credit Note](actions/retrieve-credit-note.md) | `GET /v1/credit-notes/:id` | [docs](https://developers.lexware.io/docs/#credit-notes-endpoint-retrieve-a-credit-note) |
| [Retrieve Invoice](actions/retrieve-invoice.md) | `GET /v1/invoices/:id` | [docs](https://developers.lexware.io/docs/#invoices-endpoint-retrieve-an-invoice) |
| [Retrieve Order Confirmation](actions/retrieve-order-confirmation.md) | `GET /v1/order-confirmations/:id` | [docs](https://developers.lexware.io/docs/#order-confirmations-endpoint-retrieve-an-order-confirmation) |
| [Retrieve Profile Information](actions/retrieve-profile-information.md) | `GET /v1/profile` | [docs](https://developers.lexware.io/docs/#profile-endpoint) |
| [Retrieve Quotation](actions/retrieve-quotation.md) | `GET /v1/quotations/:id` | [docs](https://developers.lexware.io/docs/#quotations-endpoint-retrieve-a-quotation) |
| [Retrieve Voucher](actions/retrieve-voucher.md) | `GET /v1/vouchers/:id` | [docs](https://developers.lexware.io/docs/#vouchers-endpoint-retrieve-a-voucher) |
| [Retrieve Voucher Payments](actions/retrieve-voucher-payments.md) | `GET /v1/payments/:voucherId` | [docs](https://developers.lexware.io/docs/#payments-endpoint-retrieve-payment-information) |
| [Update Article](actions/update-article.md) | `PUT /v1/articles/:id` | [docs](https://developers.lexware.io/docs/#articles-endpoint-update-an-article) |
| [Update Contact](actions/update-contact.md) | `PUT /v1/contacts/:id` | [docs](https://developers.lexware.io/docs/#contacts-endpoint-update-a-contact) |
| [Update Voucher](actions/update-voucher.md) | `PUT /v1/vouchers/:id` | [docs](https://developers.lexware.io/docs/#vouchers-endpoint-update-a-voucher) |
| [Upload File](actions/upload-file.md) | `POST /v1/files` | [docs](https://developers.lexware.io/docs/#files-endpoint-upload-a-file) |
| [Upload File to Voucher](actions/upload-file-to-voucher.md) | `POST /v1/vouchers/:id/files` | [docs](https://developers.lexware.io/docs/#vouchers-endpoint-upload-a-file-to-a-voucher) |
