# Veryfi OCR: Native API Reference

A consolidated summary of Veryfi OCR's API configuration and 76 documented operations, with links to official documentation.

- **Official docs:** https://docs.veryfi.com/
- **OpenAPI specification:** https://api.veryfi.com/api/v8/partner/documents/schema
- **API base URL:** `https://api.veryfi.com/`

## Authentication

### Veryfi API Signature Auth

Custom Veryfi auth using CLIENT-ID, apikey username:key authorization header, request timestamp, and HMAC signature.

### Credentials

- **Client ID:** `clientId` · required · Veryfi tenant Client ID used in the CLIENT-ID header.
- **Auth Username:** `username` · required · Veryfi auth username used in the apikey authorization header.
- **API Key:** `apiKey` · required · Veryfi API key used in the apikey authorization header.
- **Client Secret:** `clientSecret` · optional · Veryfi client secret used to compute X-VERYFI-REQUEST-SIGNATURE.

Send these headers with each API request:

```http
CLIENT-ID: <clientId>
```

[Official authentication documentation](https://docs.veryfi.com/api/getting-started/authentication/)

## API conventions

Response data is read from `documents`. The total page count is read from `meta.total_pages`. The current page number is read from `meta.page_number`.

## Pagination

Use `page_size` in the query string to set the page size (default 50; accepted range 1–50). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `order_by` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (76 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Tag To Document](actions/add-tag-to-document.md) | `PUT /api/v8/partner/documents/:document_id/tags` | [docs](https://docs.veryfi.com/api/receipts-invoices/add-a-tag-to-a-document/) |
| [Add Tags To Document](actions/add-tags-to-document.md) | `POST /api/v8/partner/documents/:document_id/tags` | [docs](https://docs.veryfi.com/api/receipts-invoices/add-a-tag-to-a-document/) |
| [Add Webhook](actions/add-webhook.md) | `POST /api/v8/partner/settings/webhooks` | [docs](https://docs.veryfi.com/api/settings/add-a-webhook/) |
| [Bulk Process Documents](actions/bulk-process-documents.md) | `POST /api/v8/partner/documents/bulk` | [docs](https://docs.veryfi.com/api/receipts-invoices/bulk-process-multiple-documents/) |
| [Classify Document](actions/classify-document.md) | `POST /api/v8/partner/classify` | [docs](https://docs.veryfi.com/api/classify/classify-a-document/) |
| [Confirm Webhook](actions/confirm-webhook.md) | `POST /api/v8/partner/settings/webhooks/confirm` | [docs](https://docs.veryfi.com/api/settings/confirm-a-webhook/) |
| [Convert Document To Markdown](actions/convert-document-to-markdown.md) | `POST /api/v8/partner/document-to-markdown` | [docs](https://docs.veryfi.com/api/document-to-markdown/convert-a-document-to-markdown/) |
| [Create Document Line Item](actions/create-document-line-item.md) | `POST /api/v8/partner/documents/:document_id/line-items` | [docs](https://docs.veryfi.com/api/receipts-invoices/create-a-line-item/) |
| [Delete All Document Line Items](actions/delete-all-document-line-items.md) | `DELETE /api/v8/partner/documents/:document_id/line-items` | [docs](https://docs.veryfi.com/api/receipts-invoices/get-a-document/) |
| [Delete AnyDoc](actions/delete-any-doc.md) | `DELETE /api/v8/partner/any-documents/:document_id` | [docs](https://docs.veryfi.com/api/anydocs/delete-a-A-doc/) |
| [Delete Bank Statement](actions/delete-bank-statement.md) | `DELETE /api/v8/partner/bank-statements/:document_id` | [docs](https://docs.veryfi.com/api/bank-statements/delete-a-bank-statement/) |
| [Delete Business Card](actions/delete-business-card.md) | `DELETE /api/v8/partner/business-cards/:document_id` | [docs](https://docs.veryfi.com/api/business-cards/delete-a-business-card/) |
| [Delete Check](actions/delete-check.md) | `DELETE /api/v8/partner/checks/:document_id` | [docs](https://docs.veryfi.com/api/checks/delete-a-check/) |
| [Delete Contract](actions/delete-contract.md) | `DELETE /api/v8/partner/contracts/:document_id` | [docs](https://docs.veryfi.com/api/contracts/delete-a-contract/) |
| [Delete Document](actions/delete-document.md) | `DELETE /api/v8/partner/documents/:document_id` | [docs](https://docs.veryfi.com/api/receipts-invoices/delete-a-document/) |
| [Delete Document Line Item](actions/delete-document-line-item.md) | `DELETE /api/v8/partner/documents/:document_id/line-items/:line_item_id` | [docs](https://docs.veryfi.com/api/receipts-invoices/get-a-document/) |
| [Delete Markdown Document](actions/delete-markdown-document.md) | `DELETE /api/v8/partner/document-to-markdown/:document_id` | [docs](https://docs.veryfi.com/api/document-to-markdown/delete-a-markdown-document/) |
| [Delete W-2](actions/delete-w2.md) | `DELETE /api/v8/partner/w2s/:document_id` | [docs](https://docs.veryfi.com/api/w2s/delete-a-w-2/) |
| [Delete W-8BEN-E](actions/delete-w8ben-e.md) | `DELETE /api/v8/partner/w-8ben-e/:document_id` | [docs](https://docs.veryfi.com/api/w-8ben-e/delete-a-w-8-ben-e/) |
| [Delete W-9](actions/delete-w9.md) | `DELETE /api/v8/partner/w9s/:document_id` | [docs](https://docs.veryfi.com/api/w9s/delete-a-w-9/) |
| [Get AnyDoc](actions/get-any-doc.md) | `GET /api/v8/partner/any-documents/:document_id` | [docs](https://docs.veryfi.com/api/anydocs/get-a-A-doc/) |
| [Get AnyDocs](actions/get-any-docs.md) | `GET /api/v8/partner/any-documents` | [docs](https://docs.veryfi.com/api/anydocs/get-A-docs/) |
| [Get Bank Statement](actions/get-bank-statement.md) | `GET /api/v8/partner/bank-statements/:document_id` | [docs](https://docs.veryfi.com/api/bank-statements/get-a-bank-statement/) |
| [Get Bank Statements](actions/get-bank-statements.md) | `GET /api/v8/partner/bank-statements` | [docs](https://docs.veryfi.com/api/bank-statements/get-bank-statements/) |
| [Get Business Card](actions/get-business-card.md) | `GET /api/v8/partner/business-cards/:document_id` | [docs](https://docs.veryfi.com/api/business-cards/get-a-business-card/) |
| [Get Business Cards](actions/get-business-cards.md) | `GET /api/v8/partner/business-cards` | [docs](https://docs.veryfi.com/api/business-cards/get-business-cards/) |
| [Get Check](actions/get-check.md) | `GET /api/v8/partner/checks/:document_id` | [docs](https://docs.veryfi.com/api/checks/get-a-check/) |
| [Get Checks](actions/get-checks.md) | `GET /api/v8/partner/checks` | [docs](https://docs.veryfi.com/api/checks/get-checks/) |
| [Get Contract](actions/get-contract.md) | `GET /api/v8/partner/contracts/:document_id` | [docs](https://docs.veryfi.com/api/contracts/get-a-contract/) |
| [Get Contracts](actions/get-contracts.md) | `GET /api/v8/partner/contracts` | [docs](https://docs.veryfi.com/api/contracts/get-contracts/) |
| [Get Document](actions/get-document.md) | `GET /api/v8/partner/documents/:document_id` | [docs](https://docs.veryfi.com/api/receipts-invoices/get-a-document/) |
| [Get Document Line Item](actions/get-document-line-item.md) | `GET /api/v8/partner/documents/:document_id/line-items/:line_item_id` | [docs](https://docs.veryfi.com/api/receipts-invoices/get-a-document/) |
| [Get Document Line Items](actions/get-document-line-items.md) | `GET /api/v8/partner/documents/:document_id/line-items` | [docs](https://docs.veryfi.com/api/receipts-invoices/get-a-document/) |
| [Get Document Tags](actions/get-document-tags.md) | `GET /api/v8/partner/documents/:document_id/tags` | [docs](https://docs.veryfi.com/api/receipts-invoices/add-a-tag-to-a-document/) |
| [Get Markdown Document](actions/get-markdown-document.md) | `GET /api/v8/partner/document-to-markdown/:document_id` | [docs](https://docs.veryfi.com/api/document-to-markdown/get-a-markdown-document/) |
| [Get Markdown Documents](actions/get-markdown-documents.md) | `GET /api/v8/partner/document-to-markdown` | [docs](https://docs.veryfi.com/api/document-to-markdown/get-markdown-documents/) |
| [Get OpenAPI Schema](actions/get-open-api-schema.md) | `GET /api/v8/partner/documents/schema` | [docs](https://docs.veryfi.com/api/get-open-api-schema/) |
| [Get W-2](actions/get-w2.md) | `GET /api/v8/partner/w2s/:document_id` | [docs](https://docs.veryfi.com/api/w2s/get-a-w-2/) |
| [Get W-2s](actions/get-w2s.md) | `GET /api/v8/partner/w2s` | [docs](https://docs.veryfi.com/api/w2s/get-w-2-s/) |
| [Get W-8BEN-E](actions/get-w8ben-e.md) | `GET /api/v8/partner/w-8ben-e/:document_id` | [docs](https://docs.veryfi.com/api/w-8ben-e/get-a-w-8-ben-e/) |
| [Get W-8BEN-Es](actions/get-w8ben-es.md) | `GET /api/v8/partner/w-8ben-e` | [docs](https://docs.veryfi.com/api/w-8ben-e/get-w-8-ben-es/) |
| [Get W-9](actions/get-w9.md) | `GET /api/v8/partner/w9s/:document_id` | [docs](https://docs.veryfi.com/api/w9s/get-a-w-9/) |
| [Get W-9s](actions/get-w9s.md) | `GET /api/v8/partner/w9s` | [docs](https://docs.veryfi.com/api/w9s/get-w-9-s/) |
| [List Webhooks](actions/list-webhooks.md) | `GET /api/v8/partner/settings/webhooks` | [docs](https://docs.veryfi.com/api/settings/get-webhooks/) |
| [Process AnyDoc](actions/process-any-doc.md) | `POST /api/v8/partner/any-documents` | [docs](https://docs.veryfi.com/api/anydocs/process-a-A-doc/) |
| [Process AnyDoc Asynchronously](actions/process-any-doc-async.md) | `POST /api/v8/partner/any-documents/async` | [docs](https://docs.veryfi.com/api/anydocs/process-a-A-doc-asynchronously/) |
| [Process Bank Statement](actions/process-bank-statement.md) | `POST /api/v8/partner/bank-statements` | [docs](https://docs.veryfi.com/api/bank-statements/process-a-bank-statement/) |
| [Process Bank Statement Asynchronously](actions/process-bank-statement-async.md) | `POST /api/v8/partner/bank-statements/async` | [docs](https://docs.veryfi.com/api/bank-statements/process-a-bank-statement-asynchronously/) |
| [Process Business Card](actions/process-business-card.md) | `POST /api/v8/partner/business-cards` | [docs](https://docs.veryfi.com/api/business-cards/process-a-business-card/) |
| [Process Check](actions/process-check.md) | `POST /api/v8/partner/checks` | [docs](https://docs.veryfi.com/api/checks/process-a-check/) |
| [Process Check Asynchronously](actions/process-check-async.md) | `POST /api/v8/partner/checks/async` | [docs](https://docs.veryfi.com/api/checks/process-a-check-asynchronously/) |
| [Process Check With Remittance](actions/process-check-with-remittance.md) | `POST /api/v8/partner/check-with-document` | [docs](https://docs.veryfi.com/api/checks/process-a-check-with-remittance/) |
| [Process Contract](actions/process-contract.md) | `POST /api/v8/partner/contracts` | [docs](https://docs.veryfi.com/api/contracts/process-a-contract/) |
| [Process Document](actions/process-document.md) | `POST /api/v8/partner/documents` | [docs](https://docs.veryfi.com/api/receipts-invoices/process-a-document/) |
| [Process Markdown Document Asynchronously](actions/process-markdown-document-async.md) | `POST /api/v8/partner/document-to-markdown/async` | [docs](https://docs.veryfi.com/api/document-to-markdown/process-a-markdown-document-asynchronously/) |
| [Process Markdown Document Set](actions/process-markdown-document-set.md) | `POST /api/v8/partner/document-to-markdown-set` | [docs](https://docs.veryfi.com/api/document-to-markdown/process-a-markdown-document-set/) |
| [Process W-2](actions/process-w2.md) | `POST /api/v8/partner/w2s` | [docs](https://docs.veryfi.com/api/w2s/process-a-w-2/) |
| [Process W-8BEN-E](actions/process-w8ben-e.md) | `POST /api/v8/partner/w-8ben-e` | [docs](https://docs.veryfi.com/api/w-8ben-e/process-a-w-8-ben-e/) |
| [Process W-9](actions/process-w9.md) | `POST /api/v8/partner/w9s` | [docs](https://docs.veryfi.com/api/w9s/process-a-w-9/) |
| [Search Documents](actions/search-documents.md) | `GET /api/v8/partner/documents` | [docs](https://docs.veryfi.com/api/receipts-invoices/search-documents/) |
| [Split And Process Bank Statements](actions/split-and-process-bank-statements.md) | `POST /api/v8/partner/bank-statements-set` | [docs](https://docs.veryfi.com/api/split-and-process-multiple-bank-statements/) |
| [Split And Process PDF](actions/split-and-process-pdf.md) | `POST /api/v8/partner/documents-set` | [docs](https://docs.veryfi.com/api/receipts-invoices/split-and-process-a-pdf/) |
| [Split And Process W-2 PDF](actions/split-and-process-w2-pdf.md) | `POST /api/v8/partner/w2s-set` | [docs](https://docs.veryfi.com/api/split-and-process-a-pdf-with-multiple-w-2-s/) |
| [Unlink All Tags From Document](actions/unlink-all-tags-from-document.md) | `DELETE /api/v8/partner/documents/:document_id/tags` | [docs](https://docs.veryfi.com/api/receipts-invoices/add-a-tag-to-a-document/) |
| [Unlink Tag From Document](actions/unlink-tag-from-document.md) | `DELETE /api/v8/partner/documents/:document_id/tags/:tag_id` | [docs](https://docs.veryfi.com/api/receipts-invoices/add-a-tag-to-a-document/) |
| [Update AnyDoc](actions/update-any-doc.md) | `PUT /api/v8/partner/any-documents/:document_id` | [docs](https://docs.veryfi.com/api/anydocs/update-a-A-doc/) |
| [Update Bank Statement](actions/update-bank-statement.md) | `PUT /api/v8/partner/bank-statements/:document_id` | [docs](https://docs.veryfi.com/api/bank-statements/update-a-bank-statement/) |
| [Update Business Card](actions/update-business-card.md) | `PUT /api/v8/partner/business-cards/:document_id` | [docs](https://docs.veryfi.com/api/business-cards/update-a-business-card/) |
| [Update Check](actions/update-check.md) | `PUT /api/v8/partner/checks/:document_id` | [docs](https://docs.veryfi.com/api/checks/update-a-check/) |
| [Update Contract](actions/update-contract.md) | `PUT /api/v8/partner/contracts/:document_id` | [docs](https://docs.veryfi.com/api/contracts/update-a-contract/) |
| [Update Document](actions/update-document.md) | `PUT /api/v8/partner/documents/:document_id` | [docs](https://docs.veryfi.com/api/receipts-invoices/update-a-document/) |
| [Update Document Line Item](actions/update-document-line-item.md) | `PUT /api/v8/partner/documents/:document_id/line-items/:line_item_id` | [docs](https://docs.veryfi.com/api/receipts-invoices/create-a-line-item/) |
| [Update Markdown Document](actions/update-markdown-document.md) | `PUT /api/v8/partner/document-to-markdown/:document_id` | [docs](https://docs.veryfi.com/api/document-to-markdown/update-a-markdown-document/) |
| [Update W-2](actions/update-w2.md) | `PUT /api/v8/partner/w2s/:document_id` | [docs](https://docs.veryfi.com/api/w2s/update-a-w-2/) |
| [Update W-8BEN-E](actions/update-w8ben-e.md) | `PUT /api/v8/partner/w-8ben-e/:document_id` | [docs](https://docs.veryfi.com/api/w-8ben-e/update-a-w-8-ben-e/) |
| [Update W-9](actions/update-w9.md) | `PUT /api/v8/partner/w9s/:document_id` | [docs](https://docs.veryfi.com/api/w9s/update-a-w-9/) |
