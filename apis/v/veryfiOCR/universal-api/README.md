# <img src="https://images.mindcloud.co/apps/icons/veryfi-icon-square_1776110307623.png" alt="Veryfi OCR logo" width="28" height="28"> Veryfi OCR: Universal API

Veryfi OCR provides OCR and data extraction APIs for receipts, invoices, checks, business cards, contracts, bank statements, tax forms, generic documents, classification, webhooks, and document-to-markdown workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/veryfiOCR/latest
- **Actions:** 76
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.veryfi.com/
- **Vendor API docs:** https://docs.veryfi.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Documents](actions/search-documents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veryfiOCR/latest/actions/search-documents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (76)

### Contracts

| Action | Method | Description |
| --- | --- | --- |
| [Delete Contract](actions/delete-contract.md) | DELETE | Deletes a contract from Veryfi OCR. |
| [Get Contract](actions/get-contract.md) | GET | Retrieves a contract from Veryfi OCR. |
| [Get Contracts](actions/get-contracts.md) | GET | Retrieves contracts from Veryfi OCR. |
| [Process Contract](actions/process-contract.md) | POST | Processes a contract in Veryfi OCR. |
| [Update Contract](actions/update-contract.md) | PUT | Updates a contract in Veryfi OCR. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Add Tag To Document](actions/add-tag-to-document.md) | PUT | Adds a tag to a document in Veryfi OCR. |
| [Add Tags To Document](actions/add-tags-to-document.md) | POST | Adds tags to a document in Veryfi OCR. |
| [Add Webhook](actions/add-webhook.md) | POST | Creates a webhook in Veryfi OCR. |
| [Bulk Process Documents](actions/bulk-process-documents.md) | POST | Processes multiple documents in Veryfi OCR. |
| [Classify Document](actions/classify-document.md) | POST | Classifies a document in Veryfi OCR. |
| [Confirm Webhook](actions/confirm-webhook.md) | POST | Confirms a webhook in Veryfi OCR. |
| [Convert Document To Markdown](actions/convert-document-to-markdown.md) | POST | Converts a document to markdown in Veryfi OCR. |
| [Create Document Line Item](actions/create-document-line-item.md) | POST | Creates a document line item in Veryfi OCR. |
| [Delete All Document Line Items](actions/delete-all-document-line-items.md) | DELETE | Deletes all document line items from Veryfi OCR. |
| [Delete AnyDoc](actions/delete-any-doc.md) | DELETE | Deletes an AnyDoc from Veryfi OCR. |
| [Delete Bank Statement](actions/delete-bank-statement.md) | DELETE | Deletes a bank statement from Veryfi OCR. |
| [Delete Business Card](actions/delete-business-card.md) | DELETE | Deletes a business card from Veryfi OCR. |
| [Delete Check](actions/delete-check.md) | DELETE | Deletes a check from Veryfi OCR. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes a document from Veryfi OCR. |
| [Delete Document Line Item](actions/delete-document-line-item.md) | DELETE | Deletes a document line item from Veryfi OCR. |
| [Delete Markdown Document](actions/delete-markdown-document.md) | DELETE | Deletes a markdown document from Veryfi OCR. |
| [Delete W-2](actions/delete-w2.md) | DELETE | Deletes a W-2 from Veryfi OCR. |
| [Delete W-8BEN-E](actions/delete-w8ben-e.md) | DELETE | Deletes a W-8BEN-E from Veryfi OCR. |
| [Delete W-9](actions/delete-w9.md) | DELETE | Deletes a W-9 from Veryfi OCR. |
| [Get AnyDoc](actions/get-any-doc.md) | GET | Retrieves an AnyDoc from Veryfi OCR. |
| [Get AnyDocs](actions/get-any-docs.md) | GET | Retrieves AnyDocs from Veryfi OCR. |
| [Get Bank Statement](actions/get-bank-statement.md) | GET | Retrieves a bank statement from Veryfi OCR. |
| [Get Bank Statements](actions/get-bank-statements.md) | GET | Retrieves bank statements from Veryfi OCR. |
| [Get Business Card](actions/get-business-card.md) | GET | Retrieves a business card from Veryfi OCR. |
| [Get Business Cards](actions/get-business-cards.md) | GET | Retrieves business cards from Veryfi OCR. |
| [Get Check](actions/get-check.md) | GET | Retrieves a check from Veryfi OCR. |
| [Get Checks](actions/get-checks.md) | GET | Retrieves checks from Veryfi OCR. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from Veryfi OCR. |
| [Get Document Line Item](actions/get-document-line-item.md) | GET | Retrieves a document line item from Veryfi OCR. |
| [Get Document Line Items](actions/get-document-line-items.md) | GET | Retrieves document line items from Veryfi OCR. |
| [Get Document Tags](actions/get-document-tags.md) | GET | Retrieves document tags from Veryfi OCR. |
| [Get Markdown Document](actions/get-markdown-document.md) | GET | Retrieves a markdown document from Veryfi OCR. |
| [Get Markdown Documents](actions/get-markdown-documents.md) | GET | Retrieves markdown documents from Veryfi OCR. |
| [Get OpenAPI Schema](actions/get-open-api-schema.md) | GET | Retrieves the OpenAPI schema from Veryfi OCR. |
| [Get W-2](actions/get-w2.md) | GET | Retrieves a W-2 from Veryfi OCR. |
| [Get W-2s](actions/get-w2s.md) | GET | Retrieves W-2s from Veryfi OCR. |
| [Get W-8BEN-E](actions/get-w8ben-e.md) | GET | Retrieves a W-8BEN-E from Veryfi OCR. |
| [Get W-8BEN-Es](actions/get-w8ben-es.md) | GET | Retrieves W-8BEN-Es from Veryfi OCR. |
| [Get W-9](actions/get-w9.md) | GET | Retrieves a W-9 from Veryfi OCR. |
| [Get W-9s](actions/get-w9s.md) | GET | Retrieves W-9s from Veryfi OCR. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Veryfi OCR. |
| [Process AnyDoc](actions/process-any-doc.md) | POST | Processes an AnyDoc in Veryfi OCR. |
| [Process AnyDoc Asynchronously](actions/process-any-doc-async.md) | POST | Processes an AnyDoc asynchronously in Veryfi OCR. |
| [Process Bank Statement](actions/process-bank-statement.md) | POST | Processes a bank statement in Veryfi OCR. |
| [Process Bank Statement Asynchronously](actions/process-bank-statement-async.md) | POST | Processes a bank statement asynchronously in Veryfi OCR. |
| [Process Business Card](actions/process-business-card.md) | POST | Processes a business card in Veryfi OCR. |
| [Process Check](actions/process-check.md) | POST | Processes a check in Veryfi OCR. |
| [Process Check Asynchronously](actions/process-check-async.md) | POST | Processes a check asynchronously in Veryfi OCR. |
| [Process Check With Remittance](actions/process-check-with-remittance.md) | POST | Processes a check with remittance in Veryfi OCR. |
| [Process Document](actions/process-document.md) | POST | Processes a document in Veryfi OCR. |
| [Process Markdown Document Asynchronously](actions/process-markdown-document-async.md) | POST | Processes a markdown document asynchronously in Veryfi OCR. |
| [Process Markdown Document Set](actions/process-markdown-document-set.md) | POST | Processes a markdown document set in Veryfi OCR. |
| [Process W-2](actions/process-w2.md) | POST | Processes a W-2 in Veryfi OCR. |
| [Process W-8BEN-E](actions/process-w8ben-e.md) | POST | Processes a W-8BEN-E in Veryfi OCR. |
| [Process W-9](actions/process-w9.md) | POST | Processes a W-9 in Veryfi OCR. |
| [Search Documents](actions/search-documents.md) | GET | Finds documents in Veryfi OCR. |
| [Split And Process Bank Statements](actions/split-and-process-bank-statements.md) | POST | Processes split bank statements in Veryfi OCR. |
| [Split And Process PDF](actions/split-and-process-pdf.md) | POST | Processes documents from a split PDF in Veryfi OCR. |
| [Split And Process W-2 PDF](actions/split-and-process-w2-pdf.md) | POST | Processes W-2s from a split PDF in Veryfi OCR. |
| [Unlink All Tags From Document](actions/unlink-all-tags-from-document.md) | DELETE | Unlinks all tags from a document in Veryfi OCR. |
| [Unlink Tag From Document](actions/unlink-tag-from-document.md) | DELETE | Unlinks a tag from a document in Veryfi OCR. |
| [Update AnyDoc](actions/update-any-doc.md) | PUT | Updates an AnyDoc in Veryfi OCR. |
| [Update Bank Statement](actions/update-bank-statement.md) | PUT | Updates a bank statement in Veryfi OCR. |
| [Update Business Card](actions/update-business-card.md) | PUT | Updates a business card in Veryfi OCR. |
| [Update Check](actions/update-check.md) | PUT | Updates a check in Veryfi OCR. |
| [Update Document](actions/update-document.md) | PUT | Updates a document in Veryfi OCR. |
| [Update Document Line Item](actions/update-document-line-item.md) | PUT | Updates a document line item in Veryfi OCR. |
| [Update Markdown Document](actions/update-markdown-document.md) | PUT | Updates a markdown document in Veryfi OCR. |
| [Update W-2](actions/update-w2.md) | PUT | Updates a W-2 in Veryfi OCR. |
| [Update W-8BEN-E](actions/update-w8ben-e.md) | PUT | Updates a W-8BEN-E in Veryfi OCR. |
| [Update W-9](actions/update-w9.md) | PUT | Updates a W-9 in Veryfi OCR. |

