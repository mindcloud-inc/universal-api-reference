# PDF-app: Native API Reference

A consolidated summary of PDF-app's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://pdf-app.net/apidocumentation
- **API base URL:** `https://api.pdf-app.net`

## Authentication

### API Key

Use your PDF-app API key in the Authorization header for all API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://pdf-app.net/apidocumentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Watermark](actions/add-watermark.md) | `POST /waterMark` | [docs](https://pdf-app.net/apidocumentation?type=waterMark) |
| [Analyze File With AI](actions/analyze-file-with-ai.md) | `POST /ai` | [docs](https://pdf-app.net/apidocumentation?type=ai) |
| [Compress PDF](actions/compress-pdf.md) | `POST /compress_PDF` | [docs](https://pdf-app.net/apidocumentation?type=compress_PDF) |
| [Convert DOCX To PDF](actions/convert-docx-to-pdf.md) | `POST /docx_to_pdf_converter` | [docs](https://pdf-app.net/apidocumentation?type=docx_to_pdf_converter) |
| [Convert Images To PDF](actions/convert-images-to-pdf.md) | `POST /image_to_pdf` | [docs](https://pdf-app.net/apidocumentation?type=image_to_pdf) |
| [Convert PDF To DOCX](actions/convert-pdf-to-docx.md) | `POST /pdf_to_docx2` | [docs](https://pdf-app.net/apidocumentation?type=pdf_to_docx2) |
| [Convert PDF To HTML](actions/convert-pdf-to-html.md) | `POST /pdf_to_html` | [docs](https://pdf-app.net/apidocumentation?type=pdf_to_html) |
| [Convert PDF To Images](actions/convert-pdf-to-images.md) | `POST /pdf_to_image` | [docs](https://pdf-app.net/apidocumentation?type=pdf_to_image) |
| [Convert Text To Speech](actions/convert-text-to-speech.md) | `POST /text_to_voice` | [docs](https://pdf-app.net/apidocumentation?type=text_to_voice) |
| [Create PDF From HTML](actions/create-pdf-from-html.md) | `POST /html_to_pdf` | [docs](https://pdf-app.net/apidocumentation?type=html_to_pdf) |
| [Create QR Code Or Barcode](actions/create-qr-code-or-barcode.md) | `POST /qrCode` | [docs](https://pdf-app.net/apidocumentation?type=qrCode) |
| [Edit PDF](actions/edit-pdf.md) | `POST /edit_pdf` | [docs](https://pdf-app.net/apidocumentation?type=edit_pdf) |
| [Encrypt File](actions/encrypt-file.md) | `POST /encryptFileExt` | [docs](https://pdf-app.net/apidocumentation?type=encryptFileExt) |
| [Extract Data From PDF](actions/extract-data-from-pdf.md) | `POST /extract_pdf_to_data_py` | [docs](https://pdf-app.net/apidocumentation?type=extract_pdf_to_data_py) |
| [Extract PDF To Structured Data](actions/extract-pdf-to-structured-data.md) | `POST /conv_classification` | [docs](https://pdf-app.net/apidocumentation?type=conv_classification) |
| [Generate AI Image](actions/generate-ai-image.md) | `POST /ai_img_generator` | [docs](https://pdf-app.net/apidocumentation?type=ai_img_generator) |
| [Get Job Result](actions/get-job-result.md) | `GET /async_jobid_check` | [docs](https://pdf-app.net/apidocumentation?type=async_jobid_check) |
| [Merge PDFs](actions/merge-pd-fs.md) | `POST /merge_pdf` | [docs](https://pdf-app.net/apidocumentation?type=merge_pdf) |
| [Outline PDF Text](actions/outline-pdf-text.md) | `POST /pdf_outline_text` | [docs](https://pdf-app.net/apidocumentation?type=pdf_outline_text) |
| [Run OCR](actions/run-ocr.md) | `POST /ocr` | [docs](https://pdf-app.net/apidocumentation?type=ocr) |
| [Split PDF](actions/split-pdf.md) | `POST /splitt_PDF` | [docs](https://pdf-app.net/apidocumentation?type=splitt_PDF) |
| [Update PDF Password](actions/update-pdf-password.md) | `POST /passwModPDFExt` | [docs](https://pdf-app.net/apidocumentation?type=passwModPDFExt) |
| [Upload Temp File](actions/upload-temp-file.md) | `POST /uploadtempFile` | [docs](https://pdf-app.net/apidocumentation?type=uploadtempFile) |
