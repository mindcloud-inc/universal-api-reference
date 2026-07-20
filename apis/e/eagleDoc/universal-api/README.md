# <img src="https://images.mindcloud.co/apps/icons/eagle-doc_1774466389307.png" alt="Eagle Doc logo" width="28" height="28"> Eagle Doc: Universal API

Process receipts, invoices, and documents with Eagle Doc OCR

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eagleDoc/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.eagle-doc.com/en/
- **Vendor API docs:** https://www.eagle-doc.com/en/documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Month Usage](actions/get-current-month-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/get-current-month-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Bank Statement Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Parse Bank Statement](actions/parse-bank-statement.md) | POST | Creates a bank statement extraction in Eagle Doc. |

### Batch Ocr Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Any Document Batch OCR Task](actions/create-any-document-batch-ocr-task.md) | POST | Creates an any-document batch OCR task in Eagle Doc. |
| [Create Finance Document Batch OCR Task](actions/create-finance-document-batch-ocr-task.md) | POST | Creates a finance document batch OCR task in Eagle Doc. |
| [Delete Batch OCR Task](actions/delete-batch-ocr-task.md) | DELETE | Deletes an existing batch OCR task from Eagle Doc. |
| [Get Batch OCR Task](actions/get-batch-ocr-task.md) | GET | Retrieves a batch OCR task from Eagle Doc. |

### Business Card Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Parse Business Card](actions/parse-business-card.md) | POST | Creates a business card extraction in Eagle Doc. |

### Delivery Sheet Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Parse Delivery Sheet](actions/parse-delivery-sheet.md) | POST | Creates a delivery sheet extraction in Eagle Doc. |

### Document Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Process Any Document](actions/process-any-document.md) | POST | Creates an any-document extraction in Eagle Doc. |

### Document Segment

| Action | Method | Description |
| --- | --- | --- |
| [Split Document](actions/split-document.md) | POST | Creates document split segments in Eagle Doc. |

### Driving License Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Parse Driving License](actions/parse-driving-license.md) | POST | Creates a driving license extraction in Eagle Doc. |

### Employee Id Card Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Parse Employee ID Card](actions/parse-employee-id-card.md) | POST | Creates an employee ID card extraction in Eagle Doc. |

### Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Submit Corrected Extraction Feedback](actions/submit-corrected-extraction-feedback.md) | POST | Creates corrected extraction feedback in Eagle Doc. |
| [Submit Instruction-Based Feedback](actions/submit-instruction-based-feedback.md) | POST | Creates instruction-based feedback in Eagle Doc. |

### Finance Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Process Finance Document](actions/process-finance-document.md) | POST | Creates a finance document extraction in Eagle Doc. |

### Invoice Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Process Invoice](actions/process-invoice.md) | POST | Creates an invoice extraction in Eagle Doc. |

### Passport Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Parse Passport](actions/parse-passport.md) | POST | Creates a passport extraction in Eagle Doc. |

### Quota

| Action | Method | Description |
| --- | --- | --- |
| [Get Quota Summary](actions/get-quota-summary.md) | GET | Retrieves quota summary from Eagle Doc. |

### Receipt Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Process Receipt](actions/process-receipt.md) | POST | Creates a receipt extraction in Eagle Doc. |

### Request Log

| Action | Method | Description |
| --- | --- | --- |
| [List Request Logs](actions/list-request-logs.md) | GET | Retrieves API request logs from Eagle Doc. |

### Resume Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Parse Resume](actions/parse-resume.md) | POST | Creates a resume extraction in Eagle Doc. |

### Signature

| Action | Method | Description |
| --- | --- | --- |
| [Extract Signatures](actions/extract-signatures.md) | POST | Creates a signature extraction in Eagle Doc. |

### Travel Ticket Extraction

| Action | Method | Description |
| --- | --- | --- |
| [Parse Travel Ticket](actions/parse-travel-ticket.md) | POST | Creates a travel ticket extraction in Eagle Doc. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Month Usage](actions/get-current-month-usage.md) | GET | Retrieves current month usage from Eagle Doc. |

### Usage Record

| Action | Method | Description |
| --- | --- | --- |
| [Get Monthly Usage History](actions/get-monthly-usage-history.md) | GET | Retrieves monthly usage history from Eagle Doc. |

