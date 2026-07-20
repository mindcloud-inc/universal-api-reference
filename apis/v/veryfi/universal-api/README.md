# <img src="https://images.mindcloud.co/apps/icons/veryfi-icon-square_1776183472698.png" alt="Veryfi logo" width="28" height="28"> Veryfi: Universal API

Veryfi OCR and document processing API for receipts, invoices, checks, contracts, tax forms, bank statements, markdown conversion, fraud blocklists, webhooks, and document metadata management.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/veryfi/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 99
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.veryfi.com/
- **Vendor API docs:** https://docs.veryfi.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get release notifications](actions/get-api-v1-release-notifications.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v1-release-notifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (99)

### Announcements

| Action | Method | Description |
| --- | --- | --- |
| [Get release notifications](actions/get-api-v1-release-notifications.md) | GET | Retrieves release notifications from Veryfi. |

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Delete a Tls Certificate](actions/delete-api-v8-partner-settings-tls-certificate-certificate-id.md) | DELETE | Deletes a TLS certificate from Veryfi. |
| [Get Tls Certificates](actions/get-api-v8-partner-settings-tls-certificate.md) | GET | Retrieves TLS certificates from Veryfi. |
| [Process a Tls Certificate](actions/post-api-v8-partner-settings-tls-certificate.md) | POST | Uploads a TLS certificate to Veryfi. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Delete a âDoc](actions/delete-api-v8-partner-any-documents-document-id.md) | DELETE | Deletes an AnyDoc from Veryfi. |
| [Delete a Bank Statement](actions/delete-api-v8-partner-bank-statements-document-id.md) | DELETE | Deletes a bank statement from Veryfi. |
| [Delete a Business Card](actions/delete-api-v8-partner-business-cards-document-id.md) | DELETE | Deletes a business card from Veryfi. |
| [Delete a Check](actions/delete-api-v8-partner-checks-document-id.md) | DELETE | Deletes a check from Veryfi. |
| [Delete a Contract](actions/delete-api-v8-partner-contracts-document-id.md) | DELETE | Deletes a contract from Veryfi. |
| [Delete a Markdown Document](actions/delete-api-v8-partner-document-to-markdown-document-id.md) | DELETE | Deletes a markdown document from Veryfi. |
| [Delete a Document](actions/delete-api-v8-partner-documents-document-id.md) | DELETE | Deletes a document from Veryfi. |
| [Delete all document Line Items](actions/delete-api-v8-partner-documents-document-id-line-items.md) | DELETE | Deletes all line items from a document in Veryfi. |
| [Delete a Line Item](actions/delete-api-v8-partner-documents-document-id-line-items-line-item-id.md) | DELETE | Deletes a line item from a document in Veryfi. |
| [Delete a Tax Line](actions/delete-api-v8-partner-documents-document-id-tax-lines-tax-line-id.md) | DELETE | Deletes a tax line from a document in Veryfi. |
| [Delete a W-8BEN-E](actions/delete-api-v8-partner-w-8ben-e-document-id.md) | DELETE | Deletes a W-8BEN-E from Veryfi. |
| [Delete a W-2](actions/delete-api-v8-partner-w2s-document-id.md) | DELETE | Deletes a W-2 from Veryfi. |
| [Delete a W-9](actions/delete-api-v8-partner-w9s-document-id.md) | DELETE | Deletes a W-9 from Veryfi. |
| [Get âDocs](actions/get-api-v8-partner-any-documents.md) | GET | Retrieves AnyDocs from Veryfi. |
| [Get a âDoc](actions/get-api-v8-partner-any-documents-document-id.md) | GET | Retrieves an AnyDoc from Veryfi. |
| [Get Bank Statements](actions/get-api-v8-partner-bank-statements.md) | GET | Retrieves bank statements from Veryfi. |
| [Get a Bank Statement](actions/get-api-v8-partner-bank-statements-document-id.md) | GET | Retrieves a bank statement from Veryfi. |
| [Get Bank Statement sets](actions/get-api-v8-partner-bank-statements-set.md) | GET | Retrieves bank statement sets from Veryfi. |
| [Get a Bank Statement set](actions/get-api-v8-partner-bank-statements-set-document-id.md) | GET | Retrieves a bank statement set from Veryfi. |
| [Get Business Cards](actions/get-api-v8-partner-business-cards.md) | GET | Retrieves business cards from Veryfi. |
| [Get a Business Card](actions/get-api-v8-partner-business-cards-document-id.md) | GET | Retrieves a business card from Veryfi. |
| [Get Checks](actions/get-api-v8-partner-checks.md) | GET | Retrieves checks from Veryfi. |
| [Get a Check](actions/get-api-v8-partner-checks-document-id.md) | GET | Retrieves a check from Veryfi. |
| [Get Contracts](actions/get-api-v8-partner-contracts.md) | GET | Retrieves contracts from Veryfi. |
| [Get a Contract](actions/get-api-v8-partner-contracts-document-id.md) | GET | Retrieves a contract from Veryfi. |
| [Get Markdown Documents](actions/get-api-v8-partner-document-to-markdown.md) | GET | Retrieves markdown documents from Veryfi. |
| [Get a Markdown Document](actions/get-api-v8-partner-document-to-markdown-document-id.md) | GET | Retrieves a markdown document from Veryfi. |
| [Get Markdown Document Sets](actions/get-api-v8-partner-document-to-markdown-set.md) | GET | Retrieves markdown document sets from Veryfi. |
| [Get a Markdown Document Set](actions/get-api-v8-partner-document-to-markdown-set-document-id.md) | GET | Retrieves a markdown document set from Veryfi. |
| [Search Documents](actions/get-api-v8-partner-documents.md) | GET | Finds documents in Veryfi. |
| [Get a Document](actions/get-api-v8-partner-documents-document-id.md) | GET | Retrieves a document from Veryfi. |
| [Get document Line Items](actions/get-api-v8-partner-documents-document-id-line-items.md) | GET | Retrieves line items from a document in Veryfi. |
| [Get a Line Item](actions/get-api-v8-partner-documents-document-id-line-items-line-item-id.md) | GET | Retrieves a line item from a document in Veryfi. |
| [Returns a list of document Tax Lines](actions/get-api-v8-partner-documents-document-id-tax-lines.md) | GET | Retrieves tax lines from a document in Veryfi. |
| [Returns document Tax Line](actions/get-api-v8-partner-documents-document-id-tax-lines-tax-line-id.md) | GET | Retrieves a tax line from a document in Veryfi. |
| [Get OpenAPI schema](actions/get-api-v8-partner-documents-schema.md) | GET | Retrieves the OpenAPI schema from Veryfi. |
| [Get Submitted PDF](actions/get-api-v8-partner-documents-set.md) | GET | Retrieves a submitted PDF from Veryfi. |
| [Get Documents from PDF](actions/get-api-v8-partner-documents-set-document-id.md) | GET | Retrieves documents from a PDF in Veryfi. |
| [Get W-8BEN-Es](actions/get-api-v8-partner-w-8ben-e.md) | GET | Retrieves W-8BEN-E documents from Veryfi. |
| [Get a W-8BEN-E](actions/get-api-v8-partner-w-8ben-e-document-id.md) | GET | Retrieves a W-8BEN-E from Veryfi. |
| [Get W-2s](actions/get-api-v8-partner-w2s.md) | GET | Retrieves W-2 documents from Veryfi. |
| [Get a W-2](actions/get-api-v8-partner-w2s-document-id.md) | GET | Retrieves a W-2 from Veryfi. |
| [Get W-2 sets](actions/get-api-v8-partner-w2s-set.md) | GET | Retrieves W-2 sets from Veryfi. |
| [Get a W-2 set](actions/get-api-v8-partner-w2s-set-document-id.md) | GET | Retrieves a W-2 set from Veryfi. |
| [Get W-9s](actions/get-api-v8-partner-w9s.md) | GET | Retrieves W-9 documents from Veryfi. |
| [Get a W-9](actions/get-api-v8-partner-w9s-document-id.md) | GET | Retrieves a W-9 from Veryfi. |
| [Process a âDoc](actions/post-api-v8-partner-any-documents.md) | POST | Creates a new AnyDoc in Veryfi. |
| [Process a âDoc asynchronously](actions/post-api-v8-partner-any-documents-async.md) | POST | Creates a new AnyDoc asynchronously in Veryfi. |
| [Process a Bank Statement](actions/post-api-v8-partner-bank-statements.md) | POST | Creates a new bank statement in Veryfi. |
| [Process a Bank Statement asynchronously](actions/post-api-v8-partner-bank-statements-async.md) | POST | Creates a new bank statement asynchronously in Veryfi. |
| [Split and process multiple Bank Statements](actions/post-api-v8-partner-bank-statements-set.md) | POST | Creates bank statements by splitting files in Veryfi. |
| [Process a Business Card](actions/post-api-v8-partner-business-cards.md) | POST | Creates a new business card in Veryfi. |
| [Process a Check](actions/post-api-v8-partner-checks.md) | POST | Creates a new check in Veryfi. |
| [Process a Check asynchronously](actions/post-api-v8-partner-checks-async.md) | POST | Creates a new check asynchronously in Veryfi. |
| [Classify a document](actions/post-api-v8-partner-classify.md) | POST | Classifies a document in Veryfi. |
| [Process a Contract](actions/post-api-v8-partner-contracts.md) | POST | Creates a new contract in Veryfi. |
| [Convert a Document to Markdown](actions/post-api-v8-partner-document-to-markdown.md) | POST | Creates a new markdown document in Veryfi. |
| [Process a Markdown Document asynchronously](actions/post-api-v8-partner-document-to-markdown-async.md) | POST | Creates a new markdown document asynchronously in Veryfi. |
| [Process a Markdown Document Set](actions/post-api-v8-partner-document-to-markdown-set.md) | POST | Creates markdown documents by splitting files in Veryfi. |
| [Process a Document](actions/post-api-v8-partner-documents.md) | POST | Creates a new document in Veryfi. |
| [Bulk Process Multiple Documents](actions/post-api-v8-partner-documents-bulk.md) | POST | Creates multiple documents in Veryfi. |
| [Create a Line Item](actions/post-api-v8-partner-documents-document-id-line-items.md) | POST | Creates a line item in a document in Veryfi. |
| [Create a Tax Line](actions/post-api-v8-partner-documents-document-id-tax-lines.md) | POST | Creates a tax line in a document in Veryfi. |
| [Split and process a PDF](actions/post-api-v8-partner-documents-set.md) | POST | Creates documents by splitting a PDF in Veryfi. |
| [Classify and possibly extract data from a document](actions/post-api-v8-partner-extract.md) | POST | Classifies a document and may extract data in Veryfi. |
| [Process a W-8BEN-E](actions/post-api-v8-partner-w-8ben-e.md) | POST | Creates a new W-8BEN-E in Veryfi. |
| [Process a W-2](actions/post-api-v8-partner-w2s.md) | POST | Creates a new W-2 in Veryfi. |
| [Split and process a PDF with multiple W-2s](actions/post-api-v8-partner-w2s-set.md) | POST | Creates W-2 documents by splitting a PDF in Veryfi. |
| [Process a W-9](actions/post-api-v8-partner-w9s.md) | POST | Creates a new W-9 in Veryfi. |
| [Update a âDoc](actions/put-api-v8-partner-any-documents-document-id.md) | PUT | Updates an existing AnyDoc in Veryfi. |
| [Update a Bank Statement](actions/put-api-v8-partner-bank-statements-document-id.md) | PUT | Updates an existing bank statement in Veryfi. |
| [Update a Business Card](actions/put-api-v8-partner-business-cards-document-id.md) | PUT | Updates an existing business card in Veryfi. |
| [Update a Check](actions/put-api-v8-partner-checks-document-id.md) | PUT | Updates an existing check in Veryfi. |
| [Update a Contract](actions/put-api-v8-partner-contracts-document-id.md) | PUT | Updates an existing contract in Veryfi. |
| [Update a Markdown Document](actions/put-api-v8-partner-document-to-markdown-document-id.md) | PUT | Updates an existing markdown document in Veryfi. |
| [Update a Document](actions/put-api-v8-partner-documents-document-id.md) | PUT | Updates an existing document in Veryfi. |
| [Update a Line Item](actions/put-api-v8-partner-documents-document-id-line-items-line-item-id.md) | PUT | Updates a line item in a document in Veryfi. |
| [Update a Tax Line](actions/put-api-v8-partner-documents-document-id-tax-lines-tax-line-id.md) | PUT | Updates a tax line in a document in Veryfi. |
| [Update a W-8BEN-E](actions/put-api-v8-partner-w-8ben-e-document-id.md) | PUT | Updates an existing W-8BEN-E in Veryfi. |
| [Update a W-2](actions/put-api-v8-partner-w2s-document-id.md) | PUT | Updates an existing W-2 in Veryfi. |
| [Update a W-9](actions/put-api-v8-partner-w9s-document-id.md) | PUT | Updates an existing W-9 in Veryfi. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Unlink all Tags from a Document](actions/delete-api-v8-partner-documents-document-id-tags.md) | DELETE | Deletes all tags from a document in Veryfi. |
| [Unlink a Tag from a Document](actions/delete-api-v8-partner-documents-document-id-tags-tag-id.md) | DELETE | Deletes a tag from a document in Veryfi. |
| [Get Document Tags](actions/get-api-v8-partner-documents-document-id-tags.md) | GET | Retrieves tags from a document in Veryfi. |
| [Add Tags to a Document](actions/post-api-v8-partner-documents-document-id-tags.md) | POST | Adds tags to a document in Veryfi. |
| [Add a Tag to a Document](actions/put-api-v8-partner-documents-document-id-tags.md) | PUT | Adds a tag to a document in Veryfi. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Get Blueprints](actions/get-api-v8-partner-blueprints.md) | GET | Retrieves blueprints from Veryfi. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Remove a device from blocklist](actions/delete-api-v8-partner-fraud-blocklist-device-id.md) | DELETE | Removes a device from Veryfi's blocklist. |
| [Get devices from blocklist](actions/get-api-v8-partner-fraud-blocklist.md) | GET | Retrieves blocked devices from Veryfi. |
| [Get ocr-counts](actions/get-api-v8-partner-ocr-counts.md) | GET | Retrieves OCR counts from Veryfi. |
| [Process a Check With Remittance](actions/post-api-v8-partner-check-with-document.md) | POST | Creates a new check with remittance in Veryfi. |
| [Add devices to blocklist](actions/post-api-v8-partner-fraud-blocklist.md) | POST | Adds devices to Veryfi's blocklist. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Get webhooks](actions/get-api-v8-partner-settings-webhooks.md) | GET | Retrieves webhooks from Veryfi. |
| [Add a webhook](actions/post-api-v8-partner-settings-webhooks.md) | POST | Creates a new webhook in Veryfi. |
| [Confirm a webhook](actions/post-api-v8-partner-settings-webhooks-confirm.md) | POST | Confirms a webhook in Veryfi. |

