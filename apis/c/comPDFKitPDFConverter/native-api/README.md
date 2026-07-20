# ComPDFKit PDF Converter: Native API Reference

A consolidated summary of ComPDFKit PDF Converter's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://api.compdf.com/api-reference/overview
- **API base URL:** `https://api-server.compdf.com/server`

## Authentication

### API Key

Authenticate REST requests with the ComPDF project Public Key sent in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://api.compdf.com/api-reference/authentication)

## API conventions

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Dewarp Document](actions/dewarp-document.md) | `POST /v2/process/documentAI/dewarp` | [docs](https://api.compdf.com/api-reference/overview) |
| [Document Extract](actions/document-extract.md) | `POST /v2/process/idp/documentExtract` | [docs](https://api.compdf.com/api-reference/overview) |
| [Get Asset Details](actions/get-asset-details.md) | `GET /v2/asset/info` | [docs](https://api.compdf.com/api-reference/api-list) |
| [Layout Analysis](actions/layout-analysis.md) | `POST /v2/process/documentAI/layoutAnalysis` | [docs](https://api.compdf.com/api-reference/overview) |
| [List Supported PDF Tools](actions/list-supported-pdf-tools.md) | `GET /v2/tool/support` | [docs](https://api.compdf.com/api-reference/api-list) |
| [Magic Color](actions/magic-color.md) | `POST /v2/process/documentAI/magicColor` | [docs](https://api.compdf.com/api-reference/overview) |
| [OCR Document](actions/ocr-document.md) | `POST /v2/process/documentAI/ocr` | [docs](https://api.compdf.com/api-reference/overview) |
| [PDF Compress](actions/pdf-compress.md) | `POST /v2/process/pdf/compress` | [docs](https://api.compdf.com/feature/pdf-editor-api) |
| [PDF Content Compare](actions/pdf-content-compare.md) | `POST /v2/process/pdf/contentCompare` | [docs](https://api.compdf.com/feature/pdf-editor-api) |
| [PDF Cover Compare](actions/pdf-cover-compare.md) | `POST /v2/process/pdf/coverCompare` | [docs](https://api.compdf.com/feature/pdf-editor-api) |
| [PDF Delete Pages](actions/pdf-delete-pages.md) | `POST /v2/process/pdf/delete` | [docs](https://api.compdf.com/feature/pdf-editor-api) |
| [PDF Extract Pages](actions/pdf-extract-pages.md) | `POST /v2/process/pdf/extract` | [docs](https://api.compdf.com/feature/pdf-editor-api) |
| [PDF Insert Pages](actions/pdf-insert-pages.md) | `POST /v2/process/pdf/insert` | [docs](https://api.compdf.com/feature/pdf-editor-api) |
| [PDF Merge](actions/pdf-merge.md) | `POST /v2/process/pdf/merge` | [docs](https://api.compdf.com/feature/pdf-editor-api) |
| [PDF Rotate Pages](actions/pdf-rotate-pages.md) | `POST /v2/process/pdf/rotation` | [docs](https://api.compdf.com/feature/pdf-editor-api) |
| [PDF Split](actions/pdf-split.md) | `POST /v2/process/pdf/split` | [docs](https://api.compdf.com/feature/pdf-editor-api) |
| [PDF to CSV](actions/pdf-to-csv.md) | `POST /v2/process/pdf/csv` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PDF to DOCX](actions/pdf-to-docx.md) | `POST /v2/process/pdf/docx` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PDF to Editable PDF](actions/pdf-to-editable.md) | `POST /v2/process/pdf/editable` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PDF to HTML](actions/pdf-to-html.md) | `POST /v2/process/pdf/html` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PDF to JPG](actions/pdf-to-jpg.md) | `POST /v2/process/pdf/jpg` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PDF to JSON](actions/pdf-to-json.md) | `POST /v2/process/pdf/json` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PDF to Markdown](actions/pdf-to-markdown.md) | `POST /v2/process/pdf/markdown` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PDF to PNG](actions/pdf-to-png.md) | `POST /v2/process/pdf/png` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PDF to PPTX](actions/pdf-to-pptx.md) | `POST /v2/process/pdf/pptx` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PDF to RTF](actions/pdf-to-rtf.md) | `POST /v2/process/pdf/rtf` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PDF to TXT](actions/pdf-to-txt.md) | `POST /v2/process/pdf/txt` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PDF to XLSX](actions/pdf-to-xlsx.md) | `POST /v2/process/pdf/xlsx` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [Stamp Detection](actions/stamp-detection.md) | `POST /v2/process/documentAI/detectionStamp` | [docs](https://api.compdf.com/api-reference/overview) |
| [Table Recognition](actions/table-recognition.md) | `POST /v2/process/documentAI/tableRec` | [docs](https://api.compdf.com/api-reference/overview) |
