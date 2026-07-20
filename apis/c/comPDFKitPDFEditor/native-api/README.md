# ComPDFKit PDF Editor: Native API Reference

A consolidated summary of ComPDFKit PDF Editor's API configuration and 55 documented operations, with links to official documentation.

- **Official docs:** https://api.compdf.com/api-libraries/overview
- **API base URL:** `https://api-server.compdf.com`

## Authentication

### API Key

Connect with the ComPDF project Public Key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://api.compdf.com/api-reference/authentication)

## Pagination

Use `size` in the query string to set the page size (default 10; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (55 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Watermark](actions/add-watermark.md) | `POST /server/v2/process/pdf/addWatermark` | [docs](https://api.compdf.com/api-reference/watermark-guides) |
| [CSV to PDF](actions/c-sv-to-pdf.md) | `POST /server/v2/process/csv/pdf` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [CSV to PDF Task](actions/c-sv-to-pdf-task.md) | `GET /server/v1/task/csv/pdf` | [docs](https://api.compdf.com/api-reference/api-list-async) |
| [Compression](actions/compression.md) | `POST /server/v2/process/pdf/compress` | [docs](https://api.compdf.com/api-reference/overview) |
| [Delete Watermark](actions/delete-watermark.md) | `POST /server/v2/process/pdf/delWatermark` | [docs](https://api.compdf.com/api-reference/watermark-guides) |
| [Document Extraction](actions/document-extraction.md) | `POST /server/v2/process/idp/documentExtract` | [docs](https://api.compdf.com/api-reference/overview) |
| [Document Parsing](actions/document-parsing.md) | `POST /server/v2/process/idp/documentParsing` | [docs](https://api.compdf.com/api-reference/overview) |
| [Get Asset Details](actions/get-asset-details.md) | `GET /server/v2/asset/info` | [docs](https://api.compdf.com/api-reference/api-list-presigned) |
| [Get Task List](actions/get-task-list.md) | `GET /server/v2/task/list` | [docs](https://api.compdf.com/api-reference/api-list) |
| [Get Tool Support](actions/get-tool-support.md) | `GET /server/v2/tool/support` | [docs](https://api.compdf.com/api-reference/api-list) |
| [HTML to PDF](actions/h-tml-to-pdf.md) | `POST /server/v2/process/html/pdf` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [HTML to PDF Task](actions/h-tml-to-pdf-task.md) | `GET /server/v1/task/html/pdf` | [docs](https://api.compdf.com/api-reference/api-list-async) |
| [Image Distortion Correction](actions/image-distortion-correction.md) | `POST /server/v2/process/documentAI/dewarp` | [docs](https://api.compdf.com/api-reference/overview) |
| [Image to CSV](actions/image-to-csv.md) | `POST /server/v2/process/img/csv` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [Image to Excel](actions/image-to-excel.md) | `POST /server/v2/process/img/xlsx` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [Image to HTML](actions/image-to-html.md) | `POST /server/v2/process/img/html` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [Image to JSON](actions/image-to-json.md) | `POST /server/v2/process/img/json` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [Image to PDF](actions/image-to-pdf.md) | `POST /server/v2/process/img/pdf` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [Image to PPT](actions/image-to-ppt.md) | `POST /server/v2/process/img/pptx` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [Image to RTF](actions/image-to-rtf.md) | `POST /server/v2/process/img/rtf` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [Image to TXT](actions/image-to-txt.md) | `POST /server/v2/process/img/txt` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [Image to Word](actions/image-to-word.md) | `POST /server/v2/process/img/docx` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PDF to JPG](actions/p-df-to-jpg.md) | `POST /server/v2/process/pdf/jpg` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PDF to PNG](actions/p-df-to-png.md) | `POST /server/v2/process/pdf/png` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PNG to PDF](actions/p-ng-to-pdf.md) | `POST /server/v2/process/png/pdf` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PNG to PDF Task](actions/p-ng-to-pdf-task.md) | `GET /server/v1/task/png/pdf` | [docs](https://api.compdf.com/api-reference/api-list-async) |
| [PPT to PDF](actions/p-pt-to-pdf.md) | `POST /server/v2/process/pptx/pdf` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PPT to PDF Task](actions/p-pt-to-pdf-task.md) | `GET /server/v1/task/pptx/pdf` | [docs](https://api.compdf.com/api-reference/api-list-async) |
| [PDF Delete Page](actions/pdf-delete-page.md) | `POST /server/v2/process/pdf/delete` | [docs](https://api.compdf.com/feature/pdf-editor-api) |
| [PDF Extract Page](actions/pdf-extract-page.md) | `POST /server/v2/process/pdf/extract` | [docs](https://api.compdf.com/feature/pdf-editor-api) |
| [PDF Generation](actions/pdf-generation.md) | `POST /server/v2/process/pdf/generate` | [docs](https://api.compdf.com/api-reference/pdf-generate) |
| [PDF Insert Page](actions/pdf-insert-page.md) | `POST /server/v2/process/pdf/insert` | [docs](https://api.compdf.com/api-reference/insert) |
| [PDF Rotate Page](actions/pdf-rotate-page.md) | `POST /server/v2/process/pdf/rotation` | [docs](https://api.compdf.com/feature/pdf-editor-api) |
| [PDF Specification Conversion](actions/pdf-specification-conversion.md) | `POST /server/v2/process/pdf/convertType` | [docs](https://api.compdf.com/api-reference/pdf-convertType) |
| [PDF Split](actions/pdf-split.md) | `POST /server/v2/process/pdf/split` | [docs](https://api.compdf.com/feature/pdf-editor-api) |
| [PDF to CSV](actions/pdf-to-csv.md) | `POST /server/v2/process/pdf/csv` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PDF to Editable PDF](actions/pdf-to-editable-pdf.md) | `POST /server/v2/process/pdf/editable` | [docs](https://api.compdf.com/api-reference/overview) |
| [PDF to Excel](actions/pdf-to-excel.md) | `POST /server/v2/process/pdf/xlsx` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PDF to HTML](actions/pdf-to-html.md) | `POST /server/v2/process/pdf/html` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PDF to Image](actions/pdf-to-image.md) | `POST /server/v2/process/pdf/img` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PDF to JSON](actions/pdf-to-json.md) | `POST /server/v2/process/pdf/json` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PDF to Markdown](actions/pdf-to-markdown.md) | `POST /server/v2/process/pdf/markdown` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PDF to PPT](actions/pdf-to-ppt.md) | `POST /server/v2/process/pdf/pptx` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PDF to RTF](actions/pdf-to-rtf.md) | `POST /server/v2/process/pdf/rtf` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PDF to TXT](actions/pdf-to-txt.md) | `POST /server/v2/process/pdf/txt` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [PDF to Word](actions/pdf-to-word.md) | `POST /server/v2/process/pdf/docx` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [RTF to PDF](actions/r-tf-to-pdf.md) | `POST /server/v2/process/rtf/pdf` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [RTF to PDF Task](actions/r-tf-to-pdf-task.md) | `GET /server/v1/task/rtf/pdf` | [docs](https://api.compdf.com/api-reference/api-list-async) |
| [Stamp Detection](actions/stamp-detection.md) | `POST /server/v2/process/documentAI/detectionStamp` | [docs](https://api.compdf.com/api-reference/overview) |
| [TXT to PDF](actions/t-xt-to-pdf.md) | `POST /server/v2/process/txt/pdf` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [TXT to PDF Task](actions/t-xt-to-pdf-task.md) | `GET /server/v1/task/txt/pdf` | [docs](https://api.compdf.com/api-reference/api-list-async) |
| [Table Extraction](actions/table-extraction.md) | `POST /server/v2/process/documentAI/tableRec` | [docs](https://api.compdf.com/api-reference/overview) |
| [Text Extraction](actions/text-extraction.md) | `POST /server/v2/process/documentAI/ocr` | [docs](https://api.compdf.com/api-reference/overview) |
| [Word to PDF](actions/word-to-pdf.md) | `POST /server/v2/process/docx/pdf` | [docs](https://api.compdf.com/api-reference/conversion-guides) |
| [Word to PDF Task](actions/word-to-pdf-task.md) | `GET /server/v1/task/docx/pdf` | [docs](https://api.compdf.com/api-reference/api-list-async) |
