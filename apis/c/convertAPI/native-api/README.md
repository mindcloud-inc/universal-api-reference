# ConvertAPI: Native API Reference

A consolidated summary of ConvertAPI's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.convertapi.com/
- **OpenAPI specification:** https://v2.convertapi.com/info/openapi
- **API base URL:** `https://v2.convertapi.com`

## Authentication

### API Token

Authenticate with a ConvertAPI API token using Bearer authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.convertapi.com/docs/authentication)

## API conventions

Request bodies use multipart form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

Responses from this API use JSON. Response data is read from `files`.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Image Watermark to PDF](actions/add-image-watermark-to-pdf.md) | `POST /convert/pdf/to/image-watermark` | [docs](https://www.convertapi.com/pdf-to-image-watermark) |
| [Add PDF Watermark to PDF](actions/add-pdf-watermark-to-pdf.md) | `POST /convert/pdf/to/pdf-watermark` | [docs](https://www.convertapi.com/pdf-to-pdf-watermark) |
| [Add Text Watermark to PDF](actions/add-text-watermark-to-pdf.md) | `POST /convert/pdf/to/text-watermark` | [docs](https://www.convertapi.com/pdf-to-text-watermark) |
| [Compare DOCX Files](actions/compare-docx-files.md) | `POST /convert/docx/to/compare` | [docs](https://www.convertapi.com/docx-to-compare) |
| [Compress PDF](actions/compress-pdf.md) | `POST /convert/pdf/to/compress` | [docs](https://www.convertapi.com/pdf-to-compress) |
| [Convert CSV to XLSX](actions/convert-csv-to-xlsx.md) | `POST /convert/csv/to/xlsx` | [docs](https://www.convertapi.com/csv-to-xlsx) |
| [Convert Doc to DOCX](actions/convert-doc-to-docx.md) | `POST /convert/doc/to/docx` | [docs](https://www.convertapi.com/doc-to-docx) |
| [Convert DOCX to HTML](actions/convert-docx-to-html.md) | `POST /convert/docx/to/html` | [docs](https://www.convertapi.com/docx-to-html) |
| [Convert DOCX to PDF](actions/convert-docx-to-pdf.md) | `POST /convert/docx/to/pdf` | [docs](https://www.convertapi.com/docx-to-pdf) |
| [Convert File to PDF](actions/convert-file-to-pdf.md) | `POST /convert/any/to/pdf` | [docs](https://www.convertapi.com/file-to-pdf) |
| [Convert File to Zip](actions/convert-file-to-zip.md) | `POST /convert/any/to/zip` | [docs](https://www.convertapi.com/file-to-zip) |
| [Convert HTML to PDF](actions/convert-html-to-pdf.md) | `POST /convert/html/to/pdf` | [docs](https://www.convertapi.com/html-to-pdf) |
| [Convert JPG to PDF](actions/convert-jpg-to-pdf.md) | `POST /convert/jpg/to/pdf` | [docs](https://www.convertapi.com/jpg-to-pdf) |
| [Convert MSG to PDF](actions/convert-msg-to-pdf.md) | `POST /convert/msg/to/pdf` | [docs](https://www.convertapi.com/msg-to-pdf) |
| [Convert Office to PDF](actions/convert-office-to-pdf.md) | `POST /convert/office/to/pdf` | [docs](https://www.convertapi.com/office-to-pdf) |
| [Convert PDF to DOCX](actions/convert-pdf-to-docx.md) | `POST /convert/pdf/to/docx` | [docs](https://www.convertapi.com/pdf-to-docx) |
| [Convert PDF to HTML](actions/convert-pdf-to-html.md) | `POST /convert/pdf/to/html` | [docs](https://www.convertapi.com/pdf-to-html) |
| [Convert PDF to JPG](actions/convert-pdf-to-jpg.md) | `POST /convert/pdf/to/jpg` | [docs](https://www.convertapi.com/pdf-to-jpg) |
| [Convert PDF to OCR](actions/convert-pdf-to-ocr.md) | `POST /convert/pdf/to/ocr` | [docs](https://www.convertapi.com/pdf-to-ocr) |
| [Convert PDF to PDF/A](actions/convert-pdf-to-pdfa.md) | `POST /convert/pdf/to/pdfa` | [docs](https://www.convertapi.com/pdf-to-pdfa) |
| [Convert PDF to PNG](actions/convert-pdf-to-png.md) | `POST /convert/pdf/to/png` | [docs](https://www.convertapi.com/pdf-to-png) |
| [Convert PDF to PPTX](actions/convert-pdf-to-pptx.md) | `POST /convert/pdf/to/pptx` | [docs](https://www.convertapi.com/pdf-to-pptx) |
| [Convert PDF to SVG](actions/convert-pdf-to-svg.md) | `POST /convert/pdf/to/svg` | [docs](https://www.convertapi.com/pdf-to-svg) |
| [Convert PDF to TXT](actions/convert-pdf-to-txt.md) | `POST /convert/pdf/to/txt` | [docs](https://www.convertapi.com/pdf-to-txt) |
| [Convert PDF to XLSX](actions/convert-pdf-to-xlsx.md) | `POST /convert/pdf/to/xlsx` | [docs](https://www.convertapi.com/pdf-to-xlsx) |
| [Convert PPTX to PDF](actions/convert-pptx-to-pdf.md) | `POST /convert/pptx/to/pdf` | [docs](https://www.convertapi.com/pptx-to-pdf) |
| [Convert Web to PDF](actions/convert-web-to-pdf.md) | `POST /convert/web/to/pdf` | [docs](https://www.convertapi.com/web-to-pdf) |
| [Convert XLSX to PDF](actions/convert-xlsx-to-pdf.md) | `POST /convert/xlsx/to/pdf` | [docs](https://www.convertapi.com/xlsx-to-pdf) |
| [Merge PDF Files](actions/merge-pdf-files.md) | `POST /convert/pdf/to/merge` | [docs](https://www.convertapi.com/pdf-to-merge) |
| [Split PDF](actions/split-pdf.md) | `POST /convert/pdf/to/split` | [docs](https://www.convertapi.com/pdf-to-split) |
