# Eagle Doc: Native API Reference

A consolidated summary of Eagle Doc's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.eagle-doc.com/en/documentation/
- **API base URL:** `https://de.eagle-doc.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
api-key: <apiKey>
```

[Official authentication documentation](https://www.eagle-doc.com/app/apis/#/developer/api-key)

## API conventions

The total page count is read from `totalPages`.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Any Document Batch OCR Task](actions/create-any-document-batch-ocr-task.md) | `POST /api/anydoc/extract/batch/task/v1` | [docs](https://www.eagle-doc.com/en/documentation/batch-ocr/) |
| [Create Finance Document Batch OCR Task](actions/create-finance-document-batch-ocr-task.md) | `POST /api/finance/extract/batch/task/v1` | [docs](https://www.eagle-doc.com/en/documentation/batch-ocr/) |
| [Delete Batch OCR Task](actions/delete-batch-ocr-task.md) | `DELETE /api/doc/task/v1` | [docs](https://www.eagle-doc.com/en/documentation/batch-ocr/) |
| [Extract Signatures](actions/extract-signatures.md) | `POST /api/signature/v1/extract` | [docs](https://www.eagle-doc.com/en/documentation/signature-extraction/) |
| [Get Batch OCR Task](actions/get-batch-ocr-task.md) | `GET /api/doc/task/v1` | [docs](https://www.eagle-doc.com/en/documentation/batch-ocr/) |
| [Get Current Month Usage](actions/get-current-month-usage.md) | `GET /api/usage/v1/current` | [docs](https://www.eagle-doc.com/en/documentation/usage/) |
| [Get Monthly Usage History](actions/get-monthly-usage-history.md) | `GET /api/usage/v1/monthly` | [docs](https://www.eagle-doc.com/en/documentation/usage/) |
| [Get Quota Summary](actions/get-quota-summary.md) | `GET /api/management/v1/quota` | [docs](https://www.eagle-doc.com/en/documentation/usage/) |
| [List Request Logs](actions/list-request-logs.md) | `GET /api/usage/v1/logs` | [docs](https://www.eagle-doc.com/en/documentation/usage/) |
| [Parse Bank Statement](actions/parse-bank-statement.md) | `POST /api/anydoc/v1/processing` | [docs](https://www.eagle-doc.com/en/documentation/anydoc-ocr/) |
| [Parse Business Card](actions/parse-business-card.md) | `POST /api/anydoc/v1/processing` | [docs](https://www.eagle-doc.com/en/documentation/anydoc-ocr/) |
| [Parse Delivery Sheet](actions/parse-delivery-sheet.md) | `POST /api/anydoc/v1/processing` | [docs](https://www.eagle-doc.com/en/documentation/anydoc-ocr/) |
| [Parse Driving License](actions/parse-driving-license.md) | `POST /api/anydoc/v1/processing` | [docs](https://www.eagle-doc.com/en/documentation/anydoc-ocr/) |
| [Parse Employee ID Card](actions/parse-employee-id-card.md) | `POST /api/anydoc/v1/processing` | [docs](https://www.eagle-doc.com/en/documentation/anydoc-ocr/) |
| [Parse Passport](actions/parse-passport.md) | `POST /api/anydoc/v1/processing` | [docs](https://www.eagle-doc.com/en/documentation/anydoc-ocr/) |
| [Parse Resume](actions/parse-resume.md) | `POST /api/anydoc/v1/processing` | [docs](https://www.eagle-doc.com/en/documentation/anydoc-ocr/) |
| [Parse Travel Ticket](actions/parse-travel-ticket.md) | `POST /api/anydoc/v1/processing` | [docs](https://www.eagle-doc.com/en/documentation/anydoc-ocr/) |
| [Process Any Document](actions/process-any-document.md) | `POST /api/anydoc/v1/processing` | [docs](https://www.eagle-doc.com/en/documentation/anydoc-ocr/) |
| [Process Finance Document](actions/process-finance-document.md) | `POST /api/finance/v1/processing` | [docs](https://www.eagle-doc.com/en/documentation/finance-ocr/) |
| [Process Invoice](actions/process-invoice.md) | `POST /api/invoice/v1/processing` | [docs](https://www.eagle-doc.com/en/documentation/invoice-ocr/) |
| [Process Receipt](actions/process-receipt.md) | `POST /api/receipt/v3/processing` | [docs](https://www.eagle-doc.com/en/documentation/receipt-ocr/) |
| [Split Document](actions/split-document.md) | `POST /api/doc/v1/split` | [docs](https://www.eagle-doc.com/en/documentation/anydoc-split/) |
| [Submit Corrected Extraction Feedback](actions/submit-corrected-extraction-feedback.md) | `POST /api/docu/learning` | [docs](https://www.eagle-doc.com/en/documentation/human-feedback/) |
| [Submit Instruction-Based Feedback](actions/submit-instruction-based-feedback.md) | `POST /api/docu/learning/instructions` | [docs](https://www.eagle-doc.com/en/documentation/human-feedback/) |
