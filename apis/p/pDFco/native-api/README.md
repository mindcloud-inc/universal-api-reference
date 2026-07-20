# PDF.co: Native API Reference

A consolidated summary of PDF.co's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://docs.pdf.co/api-reference
- **API base URL:** `https://api.pdf.co/v1`

## Authentication

### API Key

Authenticate requests using a PDF.co API key sent in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.pdf.co/api-reference)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Content to PDF](actions/add-content-to-pdf.md) | `POST /pdf/edit/add` | [docs](https://docs.pdf.co/api-tester/pdf-add) |
| [Add Password to PDF](actions/add-password-to-pdf.md) | `POST /pdf/security/add` | [docs](https://docs.pdf.co/api-tester/pdf-password/add) |
| [Check Background Job Status](actions/check-background-job-status.md) | `GET /job/check` | [docs](https://docs.pdf.co/api-reference/job-check) |
| [Classify Document](actions/classify-document.md) | `POST /pdf/classifier` | [docs](https://docs.pdf.co/api-tester/document-classifier) |
| [Compress PDF](actions/compress-pdf.md) | `POST /../v2/pdf/compress` | [docs](https://docs.pdf.co/api-tester/pdf-compress) |
| [Convert HTML to PDF](actions/convert-html-to-pdf.md) | `POST /pdf/convert/from/html` | [docs](https://docs.pdf.co/api-tester/pdf-from-html/convert) |
| [Delete Temporary File](actions/delete-temporary-file.md) | `POST /file/delete` | [docs](https://docs.pdf.co/api-reference/file-upload/delete) |
| [Excel to CSV](actions/excel-to-csv.md) | `POST /xls/convert/to/csv` | [docs](https://docs.pdf.co/api-reference/convert-from-excel/csv) |
| [Excel to PDF](actions/excel-to-pdf.md) | `POST /xls/convert/to/pdf` | [docs](https://docs.pdf.co/api-reference/convert-from-excel/pdf) |
| [Find Text in PDF](actions/find-text-in-pdf.md) | `POST /pdf/find` | [docs](https://docs.pdf.co/api-tester/pdf-find/basic) |
| [Generate Barcodes](actions/generate-barcodes.md) | `POST /barcode/generate` | [docs](https://docs.pdf.co/api-reference/barcode/generate) |
| [Get Account Balance](actions/get-account-balance.md) | `GET /account/credit/balance` | [docs](https://docs.pdf.co/api-reference/account-balance-info) |
| [Get PDF Form Fields Info](actions/get-pdf-form-fields-info.md) | `POST /pdf/info/fields` | [docs](https://docs.pdf.co/api-tester/forms/info-reader) |
| [Get PDF Info](actions/get-pdf-info.md) | `POST /pdf/info` | [docs](https://docs.pdf.co/api-tester/pdf-info-reader) |
| [List All Templates](actions/list-all-templates.md) | `GET /pdf/documentparser/templates` | [docs](https://docs.pdf.co/api-reference/documentparser/templates) |
| [Make PDF Text Searchable](actions/make-pdf-text-searchable.md) | `POST /pdf/makesearchable` | [docs](https://docs.pdf.co/api-tester/pdf-change-text-searchable/searchable) |
| [Merge PDF](actions/merge-pdf.md) | `POST /pdf/merge` | [docs](https://docs.pdf.co/api-reference/merge/pdf) |
| [Parse Document](actions/parse-document.md) | `POST /pdf/documentparser` | [docs](https://docs.pdf.co/api-reference/documentparser/parser) |
| [Parse Invoice with AI](actions/parse-invoice-with-ai.md) | `POST /ai-invoice-parser` | [docs](https://docs.pdf.co/api-tester/ai-invoice-parser) |
| [PDF Delete Pages](actions/pdf-delete-pages.md) | `POST /pdf/edit/delete-pages` | [docs](https://docs.pdf.co/api-tester/pdf-delete-pages) |
| [PDF to CSV](actions/pdf-to-csv.md) | `POST /pdf/convert/to/csv` | [docs](https://docs.pdf.co/api-tester/pdf-to-csv) |
| [PDF to HTML](actions/pdf-to-html.md) | `POST /pdf/convert/to/html` | [docs](https://docs.pdf.co/api-tester/pdf-to-html) |
| [PDF to JPG](actions/pdf-to-jpg.md) | `POST /pdf/convert/to/jpg` | [docs](https://docs.pdf.co/api-tester/pdf-to-image/jpg) |
| [PDF to JSON](actions/pdf-to-json.md) | `POST /pdf/convert/to/json2` | [docs](https://docs.pdf.co/api-tester/pdf-to-json/basic) |
| [PDF to JSON with AI](actions/pdf-to-json-with-ai.md) | `POST /pdf/convert/to/json-meta` | [docs](https://docs.pdf.co/api-reference/pdf-to-json/with-ai) |
| [PDF to PNG](actions/pdf-to-png.md) | `POST /pdf/convert/to/png` | [docs](https://docs.pdf.co/api-tester/pdf-to-image/png) |
| [PDF to Text](actions/pdf-to-text.md) | `POST /pdf/convert/to/text` | [docs](https://docs.pdf.co/api-tester/pdf-to-text/basic) |
| [PDF to XLSX](actions/pdf-to-xlsx.md) | `POST /pdf/convert/to/xlsx` | [docs](https://docs.pdf.co/api-tester/pdf-to-excel/xlsx) |
| [Read Barcodes](actions/read-barcodes.md) | `POST /barcode/read/from/url` | [docs](https://docs.pdf.co/api-reference/barcode/read) |
| [Remove Password from PDF](actions/remove-password-from-pdf.md) | `POST /pdf/security/remove` | [docs](https://docs.pdf.co/api-tester/pdf-password/remove) |
| [Rotate Selected Pages](actions/rotate-selected-pages.md) | `POST /pdf/edit/rotate` | [docs](https://docs.pdf.co/api-tester/pdf-rotate/basic) |
| [Split PDF](actions/split-pdf.md) | `POST /pdf/split` | [docs](https://docs.pdf.co/api-reference/pdf-split/by-pages) |
| [Upload File from URL](actions/upload-file-from-url.md) | `POST /file/upload/url` | [docs](https://docs.pdf.co/api-reference/file-upload/upload-url-post) |
| [Upload File Using Base64](actions/upload-file-using-base64.md) | `POST /file/upload/base64` | [docs](https://docs.pdf.co/api-reference/file-upload/upload-base64) |
