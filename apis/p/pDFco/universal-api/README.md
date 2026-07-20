# <img src="https://images.mindcloud.co/apps/icons/pdf-co_1772661583423.png" alt="PDF.co logo" width="28" height="28"> PDF.co: Universal API

Convert PDFs, extract data, merge files, and generate barcodes

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pDFco/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pdf.co
- **Vendor API docs:** https://docs.pdf.co/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Background Job Status](actions/check-background-job-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/check-background-job-status?connectionId=$CONNECTION_ID&jobid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Account Credit Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Balance](actions/get-account-balance.md) | GET | Retrieves account balance information from PDF.co. |

### Background Job

| Action | Method | Description |
| --- | --- | --- |
| [Check Background Job Status](actions/check-background-job-status.md) | GET | Retrieves a background job status from PDF.co. |

### Converted Json File

| Action | Method | Description |
| --- | --- | --- |
| [PDF to JSON](actions/pdf-to-json.md) | POST | Creates JSON data from a PDF in PDF.co. |

### Converted Text File

| Action | Method | Description |
| --- | --- | --- |
| [PDF to Text](actions/pdf-to-text.md) | POST | Creates text from a PDF in PDF.co. |

### Merged Pdf File

| Action | Method | Description |
| --- | --- | --- |
| [Merge PDF](actions/merge-pdf.md) | POST | Creates a merged PDF in PDF.co. |

### Ocr Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Make PDF Text Searchable](actions/make-pdf-text-searchable.md) | PUT | Makes a PDF text searchable in PDF.co. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Add Content to PDF](actions/add-content-to-pdf.md) | PUT | Adds content to a PDF in PDF.co. |
| [Classify Document](actions/classify-document.md) | GET | Classifies a document in PDF.co. |
| [Convert HTML to PDF](actions/convert-html-to-pdf.md) | POST | Creates a PDF from HTML in PDF.co. |
| [Excel to CSV](actions/excel-to-csv.md) | POST | Creates a CSV file from Excel in PDF.co. |
| [Excel to PDF](actions/excel-to-pdf.md) | POST | Creates a PDF from Excel in PDF.co. |
| [Generate Barcodes](actions/generate-barcodes.md) | POST | Creates barcodes in PDF.co. |
| [List All Templates](actions/list-all-templates.md) | GET | Retrieves document parser templates from PDF.co. |
| [Parse Invoice with AI](actions/parse-invoice-with-ai.md) | GET | Parses an invoice with AI in PDF.co. |
| [PDF to JSON with AI](actions/pdf-to-json-with-ai.md) | GET | Converts a PDF to JSON with AI in PDF.co. |
| [Read Barcodes](actions/read-barcodes.md) | GET | Reads barcodes from a file in PDF.co. |

### Parsed Document

| Action | Method | Description |
| --- | --- | --- |
| [Parse Document](actions/parse-document.md) | POST | Parses a document with PDF.co templates. |

### Pdf Conversion

| Action | Method | Description |
| --- | --- | --- |
| [PDF to CSV](actions/pdf-to-csv.md) | GET | Converts a PDF to CSV in PDF.co. |
| [PDF to HTML](actions/pdf-to-html.md) | GET | Converts a PDF to HTML in PDF.co. |
| [PDF to JPG](actions/pdf-to-jpg.md) | GET | Converts a PDF to JPG in PDF.co. |
| [PDF to PNG](actions/pdf-to-png.md) | GET | Converts a PDF to PNG in PDF.co. |
| [PDF to XLSX](actions/pdf-to-xlsx.md) | GET | Converts a PDF to XLSX in PDF.co. |

### Pdf Document

| Action | Method | Description |
| --- | --- | --- |
| [Compress PDF](actions/compress-pdf.md) | PUT | Compresses a PDF in PDF.co. |

### Pdf Form Fields

| Action | Method | Description |
| --- | --- | --- |
| [Get PDF Form Fields Info](actions/get-pdf-form-fields-info.md) | GET | Retrieves PDF form field info from PDF.co. |

### Pdf Info

| Action | Method | Description |
| --- | --- | --- |
| [Get PDF Info](actions/get-pdf-info.md) | GET | Retrieves PDF info from PDF.co. |

### Pdf Page Editing

| Action | Method | Description |
| --- | --- | --- |
| [PDF Delete Pages](actions/pdf-delete-pages.md) | PUT | Deletes pages from a PDF in PDF.co. |
| [Rotate Selected Pages](actions/rotate-selected-pages.md) | PUT | Rotates selected PDF pages in PDF.co. |

### Pdf Security

| Action | Method | Description |
| --- | --- | --- |
| [Add Password to PDF](actions/add-password-to-pdf.md) | PUT | Adds a password to a PDF in PDF.co. |
| [Remove Password from PDF](actions/remove-password-from-pdf.md) | PUT | Removes a password from a PDF in PDF.co. |

### Pdf Text Search

| Action | Method | Description |
| --- | --- | --- |
| [Find Text in PDF](actions/find-text-in-pdf.md) | GET | Finds text in a PDF in PDF.co. |

### Split Pdf Output

| Action | Method | Description |
| --- | --- | --- |
| [Split PDF](actions/split-pdf.md) | POST | Creates split PDF files in PDF.co. |

### Temporary File

| Action | Method | Description |
| --- | --- | --- |
| [Delete Temporary File](actions/delete-temporary-file.md) | DELETE | Deletes a temporary file from PDF.co. |

### Uploaded File

| Action | Method | Description |
| --- | --- | --- |
| [Upload File from URL](actions/upload-file-from-url.md) | POST | Uploads a file from a URL to PDF.co. |
| [Upload File Using Base64](actions/upload-file-using-base64.md) | POST | Uploads a file from Base64 to PDF.co. |

