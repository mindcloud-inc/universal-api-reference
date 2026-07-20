# <img src="https://images.mindcloud.co/apps/icons/p-dfapp_1773860802937.png" alt="PDF-app logo" width="28" height="28"> PDF-app: Universal API

Convert, extract, and automate PDF and document workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pDFApp/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pdf-app.net/
- **Vendor API docs:** https://pdf-app.net/apidocumentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Analyze File With AI](actions/analyze-file-with-ai.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/analyze-file-with-ai?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Ai Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Analyze File With AI](actions/analyze-file-with-ai.md) | GET | Retrieves AI analysis from a file in PDF-app. |

### Ai Image

| Action | Method | Description |
| --- | --- | --- |
| [Generate AI Image](actions/generate-ai-image.md) | POST | Creates an AI-generated image in PDF-app. |

### Audio

| Action | Method | Description |
| --- | --- | --- |
| [Convert Text To Speech](actions/convert-text-to-speech.md) | POST | Creates speech audio from text in PDF-app. |

### Docx

| Action | Method | Description |
| --- | --- | --- |
| [Convert PDF To DOCX](actions/convert-pdf-to-docx.md) | POST | Creates a DOCX file from a PDF in PDF-app. |

### Extraction Result

| Action | Method | Description |
| --- | --- | --- |
| [Extract Data From PDF](actions/extract-data-from-pdf.md) | GET | Retrieves extracted data from a PDF in PDF-app. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Add Watermark](actions/add-watermark.md) | PUT | Updates a PDF with a watermark in PDF-app. |
| [Encrypt File](actions/encrypt-file.md) | PUT | Updates a file with password encryption in PDF-app. |

### Html

| Action | Method | Description |
| --- | --- | --- |
| [Convert PDF To HTML](actions/convert-pdf-to-html.md) | POST | Creates HTML from a PDF in PDF-app. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Convert PDF To Images](actions/convert-pdf-to-images.md) | POST | Creates image files from a PDF in PDF-app. |
| [Create QR Code Or Barcode](actions/create-qr-code-or-barcode.md) | POST | Creates a QR code or barcode in PDF-app. |

### Job Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Result](actions/get-job-result.md) | GET | Retrieves an async job result from PDF-app. |

### Ocr Result

| Action | Method | Description |
| --- | --- | --- |
| [Run OCR](actions/run-ocr.md) | GET | Retrieves OCR text from a file in PDF-app. |

### Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Compress PDF](actions/compress-pdf.md) | POST | Creates a compressed PDF in PDF-app. |
| [Convert DOCX To PDF](actions/convert-docx-to-pdf.md) | POST | Creates a PDF from a DOCX file in PDF-app. |
| [Convert Images To PDF](actions/convert-images-to-pdf.md) | POST | Creates a PDF from image files in PDF-app. |
| [Create PDF From HTML](actions/create-pdf-from-html.md) | POST | Creates a PDF from HTML in PDF-app. |
| [Edit PDF](actions/edit-pdf.md) | PUT | Updates a PDF with edits in PDF-app. |
| [Merge PDFs](actions/merge-pd-fs.md) | POST | Creates a merged PDF in PDF-app. |
| [Outline PDF Text](actions/outline-pdf-text.md) | PUT | Updates a PDF by outlining its text in PDF-app. |
| [Split PDF](actions/split-pdf.md) | POST | Creates split PDF files in PDF-app. |
| [Update PDF Password](actions/update-pdf-password.md) | PUT | Updates a PDF password in PDF-app. |

### Structured Data

| Action | Method | Description |
| --- | --- | --- |
| [Extract PDF To Structured Data](actions/extract-pdf-to-structured-data.md) | GET | Retrieves structured data from a PDF in PDF-app. |

### Temporary File

| Action | Method | Description |
| --- | --- | --- |
| [Upload Temp File](actions/upload-temp-file.md) | POST | Creates temporary file URLs in PDF-app. |

