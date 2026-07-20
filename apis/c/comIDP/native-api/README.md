# ComIDP: Native API Reference

A consolidated summary of ComIDP's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://api.compdf.com/api-reference/overview
- **API base URL:** `https://api-server.compdf.com/server/v2`

## Authentication

### Public Key

ComPDF request authentication using the Public Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.compdf.com/api-reference/authentication)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [CSV to PDF](actions/csv-to-pdf.md) | `POST /server/v2/process/csv/pdf` | [docs](https://api.compdf.com/api-reference/csv-to-pdf) |
| [Document Extraction](actions/document-extraction.md) | `POST /server/v2/process/idp/documentExtract` | [docs](https://api.compdf.com/api-reference/documentExtract) |
| [Document Parsing](actions/document-parsing.md) | `POST /server/v2/process/idp/documentParsing` | [docs](https://api.compdf.com/api-reference/documentParsing) |
| [Excel to PDF](actions/excel-to-pdf.md) | `POST /server/v2/process/xlsx/pdf` | [docs](https://api.compdf.com/api-reference/excel-to-pdf) |
| [Get Asset Details](actions/get-asset-details.md) | `GET /server/v2/asset/info` | [docs](https://api.compdf.com/api-reference/api-list) |
| [HTML to PDF](actions/html-to-pdf.md) | `POST /server/v2/process/html/pdf` | [docs](https://api.compdf.com/api-reference/html-to-pdf) |
| [Image Distortion Correction](actions/image-distortion-correction.md) | `POST /server/v2/process/idp/imageDistortionCorrection` | [docs](https://api.compdf.com/api-reference/image-distortion-correction) |
| [Image Enhancement](actions/image-enhancement.md) | `POST /server/v2/process/idp/imageEnhancement` | [docs](https://api.compdf.com/api-reference/image-enhancement) |
| [Image to Excel](actions/image-to-excel.md) | `POST /server/v2/process/image/xlsx` | [docs](https://api.compdf.com/api-reference/image-to-excel) |
| [Image to PPT](actions/image-to-ppt.md) | `POST /server/v2/process/image/pptx` | [docs](https://api.compdf.com/api-reference/image-to-ppt) |
| [Image to TXT](actions/image-to-txt.md) | `POST /server/v2/process/image/txt` | [docs](https://api.compdf.com/api-reference/image-to-txt) |
| [Image to Word](actions/image-to-word.md) | `POST /server/v2/process/image/docx` | [docs](https://api.compdf.com/api-reference/image-to-word) |
| [PDF to CSV](actions/pdf-to-csv.md) | `POST /server/v2/process/pdf/csv` | [docs](https://api.compdf.com/api-reference/pdf-to-csv) |
| [PDF to Excel](actions/pdf-to-excel.md) | `POST /server/v2/process/pdf/xlsx` | [docs](https://api.compdf.com/api-reference/excel-to-pdf) |
| [PDF to HTML](actions/pdf-to-html.md) | `POST /server/v2/process/pdf/html` | [docs](https://api.compdf.com/api-reference/pdf-to-html) |
| [PDF to Image](actions/pdf-to-image.md) | `POST /server/v2/process/pdf/jpg` | [docs](https://api.compdf.com/api-reference/pdf-to-image) |
| [PDF to JSON](actions/pdf-to-json.md) | `POST /server/v2/process/pdf/json` | [docs](https://api.compdf.com/api-reference/json) |
| [PDF to Markdown](actions/pdf-to-markdown.md) | `POST /server/v2/process/pdf/markdown` | [docs](https://api.compdf.com/api-reference/pdf-to-markdown) |
| [PDF to PPT](actions/pdf-to-ppt.md) | `POST /server/v2/process/pdf/pptx` | [docs](https://api.compdf.com/api-reference/pdf-to-ppt) |
| [PDF to RTF](actions/pdf-to-rtf.md) | `POST /server/v2/process/pdf/rtf` | [docs](https://api.compdf.com/api-reference/pdf-to-rtf) |
| [PDF to TXT](actions/pdf-to-txt.md) | `POST /server/v2/process/pdf/txt` | [docs](https://api.compdf.com/api-reference/pdf-to-txt) |
| [PDF to Word](actions/pdf-to-word.md) | `POST /server/v2/process/pdf/docx` | [docs](https://api.compdf.com/api-reference/pdf-to-word) |
| [PNG to PDF](actions/png-to-pdf.md) | `POST /server/v2/process/png/pdf` | [docs](https://api.compdf.com/api-reference/png-to-pdf) |
| [PPT to PDF](actions/ppt-to-pdf.md) | `POST /server/v2/process/pptx/pdf` | [docs](https://api.compdf.com/api-reference/ppt-to-pdf) |
| [RTF to PDF](actions/rtf-to-pdf.md) | `POST /server/v2/process/rtf/pdf` | [docs](https://api.compdf.com/api-reference/rtf-to-pdf) |
| [Stamp Detection](actions/stamp-detection.md) | `POST /server/v2/process/idp/stampDetection` | [docs](https://api.compdf.com/api-reference/stamp-detection) |
| [Table Extraction](actions/table-extraction.md) | `POST /server/v2/process/idp/tableExtraction` | [docs](https://api.compdf.com/api-reference/table-extraction) |
| [Text Extraction](actions/text-extraction.md) | `POST /server/v2/process/idp/textExtraction` | [docs](https://api.compdf.com/api-reference/text-extraction) |
| [TXT to PDF](actions/txt-to-pdf.md) | `POST /server/v2/process/txt/pdf` | [docs](https://api.compdf.com/api-reference/txt-to-pdf) |
| [Word to PDF](actions/word-to-pdf.md) | `POST /server/v2/process/docx/pdf` | [docs](https://api.compdf.com/api-reference/word-to-pdf) |
