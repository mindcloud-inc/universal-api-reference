# Veryfi: Native API Reference

A consolidated summary of Veryfi's API configuration and 99 documented operations, with links to official documentation.

- **Official docs:** https://docs.veryfi.com/
- **OpenAPI specification:** https://docs.veryfi.com/api/veryfi-api/
- **API base URL:** `https://api.veryfi.com`

## Authentication

### Veryfi API Signature Auth

Veryfi requires CLIENT-ID, AUTHORIZATION, X-VERYFI-REQUEST-TIMESTAMP, and X-VERYFI-REQUEST-SIGNATURE on every request.

### Credentials

- **Client ID:** `clientId` · required · Veryfi client ID from the API Keys page.
- **Client Secret:** `clientSecret` · required · Veryfi client secret used to sign requests.
- **Username:** `username` · required · Veryfi API username used in the AUTHORIZATION header.
- **API Key:** `apiKey` · required · Veryfi API key paired with the username in the AUTHORIZATION header.

Send these headers with each API request:

```http
CLIENT-ID: <clientId>
```

[Official authentication documentation](https://docs.veryfi.com/api/getting-started/authentication/)

## Endpoints (99 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete a âDoc](actions/delete-api-v8-partner-any-documents-document-id.md) | `DELETE /api/v8/partner/any-documents/:document_id` | [docs](https://docs.veryfi.com/api/anydocs/delete-a-A-doc/) |
| [Delete a Bank Statement](actions/delete-api-v8-partner-bank-statements-document-id.md) | `DELETE /api/v8/partner/bank-statements/:document_id` | [docs](https://docs.veryfi.com/api/bank-statements/delete-a-bank-statement/) |
| [Delete a Business Card](actions/delete-api-v8-partner-business-cards-document-id.md) | `DELETE /api/v8/partner/business-cards/:document_id` | [docs](https://docs.veryfi.com/api/business-cards/delete-a-business-card/) |
| [Delete a Check](actions/delete-api-v8-partner-checks-document-id.md) | `DELETE /api/v8/partner/checks/:document_id` | [docs](https://docs.veryfi.com/api/checks/delete-a-check/) |
| [Delete a Contract](actions/delete-api-v8-partner-contracts-document-id.md) | `DELETE /api/v8/partner/contracts/:document_id` | [docs](https://docs.veryfi.com/api/contracts/delete-a-contract/) |
| [Delete a Markdown Document](actions/delete-api-v8-partner-document-to-markdown-document-id.md) | `DELETE /api/v8/partner/document-to-markdown/:document_id` | [docs](https://docs.veryfi.com/api/document-to-markdown/delete-a-markdown-document/) |
| [Delete a Document](actions/delete-api-v8-partner-documents-document-id.md) | `DELETE /api/v8/partner/documents/:document_id` | [docs](https://docs.veryfi.com/api/receipts-invoices/delete-a-document/) |
| [Delete all document Line Items](actions/delete-api-v8-partner-documents-document-id-line-items.md) | `DELETE /api/v8/partner/documents/:document_id/line-items` | [docs](https://docs.veryfi.com/api/receipts-invoices/delete-all-document-line-items/) |
| [Delete a Line Item](actions/delete-api-v8-partner-documents-document-id-line-items-line-item-id.md) | `DELETE /api/v8/partner/documents/:document_id/line-items/:line_item_id` | [docs](https://docs.veryfi.com/api/receipts-invoices/delete-a-line-item/) |
| [Unlink all Tags from a Document](actions/delete-api-v8-partner-documents-document-id-tags.md) | `DELETE /api/v8/partner/documents/:document_id/tags` | [docs](https://docs.veryfi.com/api/receipts-invoices/unlink-all-tags-from-a-document/) |
| [Unlink a Tag from a Document](actions/delete-api-v8-partner-documents-document-id-tags-tag-id.md) | `DELETE /api/v8/partner/documents/:document_id/tags/:tag_id` | [docs](https://docs.veryfi.com/api/receipts-invoices/unlink-a-tag-from-a-document/) |
| [Delete a Tax Line](actions/delete-api-v8-partner-documents-document-id-tax-lines-tax-line-id.md) | `DELETE /api/v8/partner/documents/:document_id/tax-lines/:tax_line_id` | [docs](https://docs.veryfi.com/api/delete-a-tax-line/) |
| [Remove a device from blocklist](actions/delete-api-v8-partner-fraud-blocklist-device-id.md) | `DELETE /api/v8/partner/fraud/blocklist/:device_id` | [docs](https://docs.veryfi.com/api/remove-a-device-from-blocklist/) |
| [Delete a Tls Certificate](actions/delete-api-v8-partner-settings-tls-certificate-certificate-id.md) | `DELETE /api/v8/partner/settings/tls-certificate/:certificate_id` | [docs](https://docs.veryfi.com/api/delete-a-tls-certificate/) |
| [Delete a W-8BEN-E](actions/delete-api-v8-partner-w-8ben-e-document-id.md) | `DELETE /api/v8/partner/w-8ben-e/:document_id` | [docs](https://docs.veryfi.com/api/w-8ben-e/delete-a-w-8-ben-e/) |
| [Delete a W-2](actions/delete-api-v8-partner-w2s-document-id.md) | `DELETE /api/v8/partner/w2s/:document_id` | [docs](https://docs.veryfi.com/api/w2s/delete-a-w-2/) |
| [Delete a W-9](actions/delete-api-v8-partner-w9s-document-id.md) | `DELETE /api/v8/partner/w9s/:document_id` | [docs](https://docs.veryfi.com/api/w9s/delete-a-w-9/) |
| [Get release notifications](actions/get-api-v1-release-notifications.md) | `GET /api/v1/release-notifications` | [docs](https://docs.veryfi.com/api/get-release-notifications/) |
| [Get âDocs](actions/get-api-v8-partner-any-documents.md) | `GET /api/v8/partner/any-documents` | [docs](https://docs.veryfi.com/api/anydocs/get-A-docs/) |
| [Get a âDoc](actions/get-api-v8-partner-any-documents-document-id.md) | `GET /api/v8/partner/any-documents/:document_id` | [docs](https://docs.veryfi.com/api/anydocs/get-a-A-doc/) |
| [Get Bank Statements](actions/get-api-v8-partner-bank-statements.md) | `GET /api/v8/partner/bank-statements` | [docs](https://docs.veryfi.com/api/bank-statements/get-bank-statements/) |
| [Get a Bank Statement](actions/get-api-v8-partner-bank-statements-document-id.md) | `GET /api/v8/partner/bank-statements/:document_id` | [docs](https://docs.veryfi.com/api/bank-statements/get-a-bank-statement/) |
| [Get Bank Statement sets](actions/get-api-v8-partner-bank-statements-set.md) | `GET /api/v8/partner/bank-statements-set` | [docs](https://docs.veryfi.com/api/get-bank-statement-sets/) |
| [Get a Bank Statement set](actions/get-api-v8-partner-bank-statements-set-document-id.md) | `GET /api/v8/partner/bank-statements-set/:document_id` | [docs](https://docs.veryfi.com/api/get-a-bank-statement-set/) |
| [Get Blueprints](actions/get-api-v8-partner-blueprints.md) | `GET /api/v8/partner/blueprints` | [docs](https://docs.veryfi.com/api/get-blueprints/) |
| [Get Business Cards](actions/get-api-v8-partner-business-cards.md) | `GET /api/v8/partner/business-cards` | [docs](https://docs.veryfi.com/api/business-cards/get-business-cards/) |
| [Get a Business Card](actions/get-api-v8-partner-business-cards-document-id.md) | `GET /api/v8/partner/business-cards/:document_id` | [docs](https://docs.veryfi.com/api/business-cards/get-a-business-card/) |
| [Get Checks](actions/get-api-v8-partner-checks.md) | `GET /api/v8/partner/checks` | [docs](https://docs.veryfi.com/api/checks/get-checks/) |
| [Get a Check](actions/get-api-v8-partner-checks-document-id.md) | `GET /api/v8/partner/checks/:document_id` | [docs](https://docs.veryfi.com/api/checks/get-a-check/) |
| [Get Contracts](actions/get-api-v8-partner-contracts.md) | `GET /api/v8/partner/contracts` | [docs](https://docs.veryfi.com/api/contracts/get-contracts/) |
| [Get a Contract](actions/get-api-v8-partner-contracts-document-id.md) | `GET /api/v8/partner/contracts/:document_id` | [docs](https://docs.veryfi.com/api/contracts/get-a-contract/) |
| [Get Markdown Documents](actions/get-api-v8-partner-document-to-markdown.md) | `GET /api/v8/partner/document-to-markdown` | [docs](https://docs.veryfi.com/api/document-to-markdown/get-markdown-documents/) |
| [Get a Markdown Document](actions/get-api-v8-partner-document-to-markdown-document-id.md) | `GET /api/v8/partner/document-to-markdown/:document_id` | [docs](https://docs.veryfi.com/api/document-to-markdown/get-a-markdown-document/) |
| [Get Markdown Document Sets](actions/get-api-v8-partner-document-to-markdown-set.md) | `GET /api/v8/partner/document-to-markdown-set` | [docs](https://docs.veryfi.com/api/document-to-markdown/get-markdown-document-sets/) |
| [Get a Markdown Document Set](actions/get-api-v8-partner-document-to-markdown-set-document-id.md) | `GET /api/v8/partner/document-to-markdown-set/:document_id` | [docs](https://docs.veryfi.com/api/document-to-markdown/get-a-markdown-document-set/) |
| [Search Documents](actions/get-api-v8-partner-documents.md) | `GET /api/v8/partner/documents` | [docs](https://docs.veryfi.com/api/receipts-invoices/search-documents/) |
| [Get a Document](actions/get-api-v8-partner-documents-document-id.md) | `GET /api/v8/partner/documents/:document_id` | [docs](https://docs.veryfi.com/api/receipts-invoices/get-a-document/) |
| [Get document Line Items](actions/get-api-v8-partner-documents-document-id-line-items.md) | `GET /api/v8/partner/documents/:document_id/line-items` | [docs](https://docs.veryfi.com/api/receipts-invoices/get-document-line-items/) |
| [Get a Line Item](actions/get-api-v8-partner-documents-document-id-line-items-line-item-id.md) | `GET /api/v8/partner/documents/:document_id/line-items/:line_item_id` | [docs](https://docs.veryfi.com/api/receipts-invoices/get-a-line-item/) |
| [Get Document Tags](actions/get-api-v8-partner-documents-document-id-tags.md) | `GET /api/v8/partner/documents/:document_id/tags` | [docs](https://docs.veryfi.com/api/receipts-invoices/get-document-tags/) |
| [Returns a list of document Tax Lines](actions/get-api-v8-partner-documents-document-id-tax-lines.md) | `GET /api/v8/partner/documents/:document_id/tax-lines` | [docs](https://docs.veryfi.com/api/returns-a-list-of-document-tax-lines/) |
| [Returns document Tax Line](actions/get-api-v8-partner-documents-document-id-tax-lines-tax-line-id.md) | `GET /api/v8/partner/documents/:document_id/tax-lines/:tax_line_id` | [docs](https://docs.veryfi.com/api/returns-document-tax-line/) |
| [Get OpenAPI schema](actions/get-api-v8-partner-documents-schema.md) | `GET /api/v8/partner/documents/schema` | [docs](https://docs.veryfi.com/api/get-open-api-schema/) |
| [Get Submitted PDF](actions/get-api-v8-partner-documents-set.md) | `GET /api/v8/partner/documents-set` | [docs](https://docs.veryfi.com/api/receipts-invoices/get-submitted-pdf/) |
| [Get Documents from PDF](actions/get-api-v8-partner-documents-set-document-id.md) | `GET /api/v8/partner/documents-set/:document_id` | [docs](https://docs.veryfi.com/api/receipts-invoices/get-documents-from-pdf/) |
| [Get devices from blocklist](actions/get-api-v8-partner-fraud-blocklist.md) | `GET /api/v8/partner/fraud/blocklist` | [docs](https://docs.veryfi.com/api/get-devices-from-blocklist/) |
| [Get ocr-counts](actions/get-api-v8-partner-ocr-counts.md) | `GET /api/v8/partner/ocr-counts` | [docs](https://docs.veryfi.com/api/get-ocr-counts/) |
| [Get Tls Certificates](actions/get-api-v8-partner-settings-tls-certificate.md) | `GET /api/v8/partner/settings/tls-certificate` | [docs](https://docs.veryfi.com/api/get-tls-certificates/) |
| [Get webhooks](actions/get-api-v8-partner-settings-webhooks.md) | `GET /api/v8/partner/settings/webhooks` | [docs](https://docs.veryfi.com/api/settings/get-webhooks/) |
| [Get W-8BEN-Es](actions/get-api-v8-partner-w-8ben-e.md) | `GET /api/v8/partner/w-8ben-e` | [docs](https://docs.veryfi.com/api/w-8ben-e/get-w-8-ben-es/) |
| [Get a W-8BEN-E](actions/get-api-v8-partner-w-8ben-e-document-id.md) | `GET /api/v8/partner/w-8ben-e/:document_id` | [docs](https://docs.veryfi.com/api/w-8ben-e/get-a-w-8-ben-e/) |
| [Get W-2s](actions/get-api-v8-partner-w2s.md) | `GET /api/v8/partner/w2s` | [docs](https://docs.veryfi.com/api/w2s/get-w-2-s/) |
| [Get a W-2](actions/get-api-v8-partner-w2s-document-id.md) | `GET /api/v8/partner/w2s/:document_id` | [docs](https://docs.veryfi.com/api/w2s/get-a-w-2/) |
| [Get W-2 sets](actions/get-api-v8-partner-w2s-set.md) | `GET /api/v8/partner/w2s-set` | [docs](https://docs.veryfi.com/api/get-w-2-sets/) |
| [Get a W-2 set](actions/get-api-v8-partner-w2s-set-document-id.md) | `GET /api/v8/partner/w2s-set/:document_id` | [docs](https://docs.veryfi.com/api/get-a-w-2-set/) |
| [Get W-9s](actions/get-api-v8-partner-w9s.md) | `GET /api/v8/partner/w9s` | [docs](https://docs.veryfi.com/api/w9s/get-w-9-s/) |
| [Get a W-9](actions/get-api-v8-partner-w9s-document-id.md) | `GET /api/v8/partner/w9s/:document_id` | [docs](https://docs.veryfi.com/api/w9s/get-a-w-9/) |
| [Process a âDoc](actions/post-api-v8-partner-any-documents.md) | `POST /api/v8/partner/any-documents` | [docs](https://docs.veryfi.com/api/anydocs/process-a-A-doc/) |
| [Process a âDoc asynchronously](actions/post-api-v8-partner-any-documents-async.md) | `POST /api/v8/partner/any-documents/async` | [docs](https://docs.veryfi.com/api/anydocs/process-a-A-doc-asynchronously/) |
| [Process a Bank Statement](actions/post-api-v8-partner-bank-statements.md) | `POST /api/v8/partner/bank-statements` | [docs](https://docs.veryfi.com/api/bank-statements/process-a-bank-statement/) |
| [Process a Bank Statement asynchronously](actions/post-api-v8-partner-bank-statements-async.md) | `POST /api/v8/partner/bank-statements/async` | [docs](https://docs.veryfi.com/api/bank-statements/process-a-bank-statement-asynchronously/) |
| [Split and process multiple Bank Statements](actions/post-api-v8-partner-bank-statements-set.md) | `POST /api/v8/partner/bank-statements-set` | [docs](https://docs.veryfi.com/api/split-and-process-multiple-bank-statements/) |
| [Process a Business Card](actions/post-api-v8-partner-business-cards.md) | `POST /api/v8/partner/business-cards` | [docs](https://docs.veryfi.com/api/business-cards/process-a-business-card/) |
| [Process a Check With Remittance](actions/post-api-v8-partner-check-with-document.md) | `POST /api/v8/partner/check-with-document` | [docs](https://docs.veryfi.com/api/checks/process-a-check-with-remittance/) |
| [Process a Check](actions/post-api-v8-partner-checks.md) | `POST /api/v8/partner/checks` | [docs](https://docs.veryfi.com/api/checks/process-a-check/) |
| [Process a Check asynchronously](actions/post-api-v8-partner-checks-async.md) | `POST /api/v8/partner/checks/async` | [docs](https://docs.veryfi.com/api/checks/process-a-check-asynchronously/) |
| [Classify a document](actions/post-api-v8-partner-classify.md) | `POST /api/v8/partner/classify` | [docs](https://docs.veryfi.com/api/classify/classify-a-document/) |
| [Process a Contract](actions/post-api-v8-partner-contracts.md) | `POST /api/v8/partner/contracts` | [docs](https://docs.veryfi.com/api/contracts/process-a-contract/) |
| [Convert a Document to Markdown](actions/post-api-v8-partner-document-to-markdown.md) | `POST /api/v8/partner/document-to-markdown` | [docs](https://docs.veryfi.com/api/document-to-markdown/convert-a-document-to-markdown/) |
| [Process a Markdown Document asynchronously](actions/post-api-v8-partner-document-to-markdown-async.md) | `POST /api/v8/partner/document-to-markdown/async` | [docs](https://docs.veryfi.com/api/document-to-markdown/process-a-markdown-document-asynchronously/) |
| [Process a Markdown Document Set](actions/post-api-v8-partner-document-to-markdown-set.md) | `POST /api/v8/partner/document-to-markdown-set` | [docs](https://docs.veryfi.com/api/document-to-markdown/process-a-markdown-document-set/) |
| [Process a Document](actions/post-api-v8-partner-documents.md) | `POST /api/v8/partner/documents` | [docs](https://docs.veryfi.com/api/receipts-invoices/process-a-document/) |
| [Bulk Process Multiple Documents](actions/post-api-v8-partner-documents-bulk.md) | `POST /api/v8/partner/documents/bulk` | [docs](https://docs.veryfi.com/api/receipts-invoices/bulk-process-multiple-documents/) |
| [Create a Line Item](actions/post-api-v8-partner-documents-document-id-line-items.md) | `POST /api/v8/partner/documents/:document_id/line-items` | [docs](https://docs.veryfi.com/api/receipts-invoices/create-a-line-item/) |
| [Add Tags to a Document](actions/post-api-v8-partner-documents-document-id-tags.md) | `POST /api/v8/partner/documents/:document_id/tags` | [docs](https://docs.veryfi.com/api/receipts-invoices/add-tags-to-a-document/) |
| [Create a Tax Line](actions/post-api-v8-partner-documents-document-id-tax-lines.md) | `POST /api/v8/partner/documents/:document_id/tax-lines` | [docs](https://docs.veryfi.com/api/create-a-tax-line/) |
| [Split and process a PDF](actions/post-api-v8-partner-documents-set.md) | `POST /api/v8/partner/documents-set` | [docs](https://docs.veryfi.com/api/receipts-invoices/split-and-process-a-pdf/) |
| [Classify and possibly extract data from a document](actions/post-api-v8-partner-extract.md) | `POST /api/v8/partner/extract` | [docs](https://docs.veryfi.com/api/classify-and-possibly-extract-data-from-a-document/) |
| [Add devices to blocklist](actions/post-api-v8-partner-fraud-blocklist.md) | `POST /api/v8/partner/fraud/blocklist` | [docs](https://docs.veryfi.com/api/add-devices-to-blocklist/) |
| [Process a Tls Certificate](actions/post-api-v8-partner-settings-tls-certificate.md) | `POST /api/v8/partner/settings/tls-certificate` | [docs](https://docs.veryfi.com/api/process-a-tls-certificate/) |
| [Add a webhook](actions/post-api-v8-partner-settings-webhooks.md) | `POST /api/v8/partner/settings/webhooks` | [docs](https://docs.veryfi.com/api/settings/add-a-webhook/) |
| [Confirm a webhook](actions/post-api-v8-partner-settings-webhooks-confirm.md) | `POST /api/v8/partner/settings/webhooks/confirm` | [docs](https://docs.veryfi.com/api/settings/confirm-a-webhook/) |
| [Process a W-8BEN-E](actions/post-api-v8-partner-w-8ben-e.md) | `POST /api/v8/partner/w-8ben-e` | [docs](https://docs.veryfi.com/api/w-8ben-e/process-a-w-8-ben-e/) |
| [Process a W-2](actions/post-api-v8-partner-w2s.md) | `POST /api/v8/partner/w2s` | [docs](https://docs.veryfi.com/api/w2s/process-a-w-2/) |
| [Split and process a PDF with multiple W-2s](actions/post-api-v8-partner-w2s-set.md) | `POST /api/v8/partner/w2s-set` | [docs](https://docs.veryfi.com/api/split-and-process-a-pdf-with-multiple-w-2-s/) |
| [Process a W-9](actions/post-api-v8-partner-w9s.md) | `POST /api/v8/partner/w9s` | [docs](https://docs.veryfi.com/api/w9s/process-a-w-9/) |
| [Update a âDoc](actions/put-api-v8-partner-any-documents-document-id.md) | `PUT /api/v8/partner/any-documents/:document_id` | [docs](https://docs.veryfi.com/api/anydocs/update-a-A-doc/) |
| [Update a Bank Statement](actions/put-api-v8-partner-bank-statements-document-id.md) | `PUT /api/v8/partner/bank-statements/:document_id` | [docs](https://docs.veryfi.com/api/bank-statements/update-a-bank-statement/) |
| [Update a Business Card](actions/put-api-v8-partner-business-cards-document-id.md) | `PUT /api/v8/partner/business-cards/:document_id` | [docs](https://docs.veryfi.com/api/business-cards/update-a-business-card/) |
| [Update a Check](actions/put-api-v8-partner-checks-document-id.md) | `PUT /api/v8/partner/checks/:document_id` | [docs](https://docs.veryfi.com/api/checks/update-a-check/) |
| [Update a Contract](actions/put-api-v8-partner-contracts-document-id.md) | `PUT /api/v8/partner/contracts/:document_id` | [docs](https://docs.veryfi.com/api/contracts/update-a-contract/) |
| [Update a Markdown Document](actions/put-api-v8-partner-document-to-markdown-document-id.md) | `PUT /api/v8/partner/document-to-markdown/:document_id` | [docs](https://docs.veryfi.com/api/document-to-markdown/update-a-markdown-document/) |
| [Update a Document](actions/put-api-v8-partner-documents-document-id.md) | `PUT /api/v8/partner/documents/:document_id` | [docs](https://docs.veryfi.com/api/receipts-invoices/update-a-document/) |
| [Update a Line Item](actions/put-api-v8-partner-documents-document-id-line-items-line-item-id.md) | `PUT /api/v8/partner/documents/:document_id/line-items/:line_item_id` | [docs](https://docs.veryfi.com/api/receipts-invoices/update-a-line-item/) |
| [Add a Tag to a Document](actions/put-api-v8-partner-documents-document-id-tags.md) | `PUT /api/v8/partner/documents/:document_id/tags` | [docs](https://docs.veryfi.com/api/receipts-invoices/add-a-tag-to-a-document/) |
| [Update a Tax Line](actions/put-api-v8-partner-documents-document-id-tax-lines-tax-line-id.md) | `PUT /api/v8/partner/documents/:document_id/tax-lines/:tax_line_id` | [docs](https://docs.veryfi.com/api/update-a-tax-line/) |
| [Update a W-8BEN-E](actions/put-api-v8-partner-w-8ben-e-document-id.md) | `PUT /api/v8/partner/w-8ben-e/:document_id` | [docs](https://docs.veryfi.com/api/w-8ben-e/update-a-w-8-ben-e/) |
| [Update a W-2](actions/put-api-v8-partner-w2s-document-id.md) | `PUT /api/v8/partner/w2s/:document_id` | [docs](https://docs.veryfi.com/api/w2s/update-a-w-2/) |
| [Update a W-9](actions/put-api-v8-partner-w9s-document-id.md) | `PUT /api/v8/partner/w9s/:document_id` | [docs](https://docs.veryfi.com/api/w9s/update-a-w-9/) |
