# <img src="https://images.mindcloud.co/apps/icons/com-pdfkit-pdfeditor_1775853244601.png" alt="ComPDFKit PDF Editor logo" width="28" height="28"> ComPDFKit PDF Editor: Universal API

Run ComPDFKit PDF Editor actions for merge, split, extract, insert, delete, rotate, watermark, compression, comparison, and document-AI workflows through the ComPDF API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/comPDFKitPDFEditor/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 55
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.compdf.com
- **Vendor API docs:** https://api.compdf.com/api-libraries/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Asset Details](actions/get-asset-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/comPDFKitPDFEditor/latest/actions/get-asset-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (55)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Get Asset Details](actions/get-asset-details.md) | GET | Retrieves remaining asset balances from ComPDFKit PDF Editor. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Get Tool Support](actions/get-tool-support.md) | GET | Retrieves supported PDF tools from ComPDFKit PDF Editor. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Add Watermark](actions/add-watermark.md) | POST | Creates a watermarking task in ComPDFKit PDF Editor. |
| [CSV to PDF](actions/c-sv-to-pdf.md) | POST | Creates a CSV-to-PDF conversion task in ComPDFKit PDF Editor. |
| [CSV to PDF Task](actions/c-sv-to-pdf-task.md) | GET |  |
| [Compression](actions/compression.md) | POST | Creates a PDF compression task in ComPDFKit PDF Editor. |
| [Delete Watermark](actions/delete-watermark.md) | POST | Creates a watermark removal task in ComPDFKit PDF Editor. |
| [Document Extraction](actions/document-extraction.md) | POST | Creates a document extraction task in ComPDFKit PDF Editor. |
| [Document Parsing](actions/document-parsing.md) | POST | Creates a document parsing task in ComPDFKit PDF Editor. |
| [Get Task List](actions/get-task-list.md) | GET | Retrieves file transfer tasks from ComPDFKit PDF Editor. |
| [HTML to PDF](actions/h-tml-to-pdf.md) | POST | Creates an HTML-to-PDF conversion task in ComPDFKit PDF Editor. |
| [HTML to PDF Task](actions/h-tml-to-pdf-task.md) | GET |  |
| [Image Distortion Correction](actions/image-distortion-correction.md) | POST | Creates an image distortion correction task in ComPDFKit PDF Editor. |
| [Image to CSV](actions/image-to-csv.md) | POST | Creates an image-to-CSV conversion task in ComPDFKit PDF Editor. |
| [Image to Excel](actions/image-to-excel.md) | POST | Creates an image-to-Excel conversion task in ComPDFKit PDF Editor. |
| [Image to HTML](actions/image-to-html.md) | POST | Creates an image-to-HTML conversion task in ComPDFKit PDF Editor. |
| [Image to JSON](actions/image-to-json.md) | POST | Creates an image-to-JSON conversion task in ComPDFKit PDF Editor. |
| [Image to PDF](actions/image-to-pdf.md) | POST | Creates an image-to-PDF conversion task in ComPDFKit PDF Editor. |
| [Image to PPT](actions/image-to-ppt.md) | POST | Creates an image-to-PPT conversion task in ComPDFKit PDF Editor. |
| [Image to RTF](actions/image-to-rtf.md) | POST | Creates an image-to-RTF conversion task in ComPDFKit PDF Editor. |
| [Image to TXT](actions/image-to-txt.md) | POST | Creates an image-to-TXT conversion task in ComPDFKit PDF Editor. |
| [Image to Word](actions/image-to-word.md) | POST | Creates an image-to-Word conversion task in ComPDFKit PDF Editor. |
| [PDF to JPG](actions/p-df-to-jpg.md) | POST | Creates a PDF-to-JPG conversion task in ComPDFKit PDF Editor. |
| [PDF to PNG](actions/p-df-to-png.md) | POST | Creates a PDF-to-PNG conversion task in ComPDFKit PDF Editor. |
| [PNG to PDF](actions/p-ng-to-pdf.md) | POST | Creates a PNG-to-PDF conversion task in ComPDFKit PDF Editor. |
| [PNG to PDF Task](actions/p-ng-to-pdf-task.md) | GET |  |
| [PPT to PDF](actions/p-pt-to-pdf.md) | POST | Creates a PPT-to-PDF conversion task in ComPDFKit PDF Editor. |
| [PPT to PDF Task](actions/p-pt-to-pdf-task.md) | GET |  |
| [PDF Delete Page](actions/pdf-delete-page.md) | POST | Creates a PDF page deletion task in ComPDFKit PDF Editor. |
| [PDF Extract Page](actions/pdf-extract-page.md) | POST | Creates a PDF page extraction task in ComPDFKit PDF Editor. |
| [PDF Generation](actions/pdf-generation.md) | POST | Creates a PDF generation task in ComPDFKit PDF Editor. |
| [PDF Insert Page](actions/pdf-insert-page.md) | POST | Creates a PDF page insertion task in ComPDFKit PDF Editor. |
| [PDF Rotate Page](actions/pdf-rotate-page.md) | POST | Creates a PDF page rotation task in ComPDFKit PDF Editor. |
| [PDF Specification Conversion](actions/pdf-specification-conversion.md) | POST | Creates a PDF specification conversion task in ComPDFKit PDF Editor. |
| [PDF Split](actions/pdf-split.md) | POST | Creates a PDF split task in ComPDFKit PDF Editor. |
| [PDF to CSV](actions/pdf-to-csv.md) | POST | Creates a PDF-to-CSV conversion task in ComPDFKit PDF Editor. |
| [PDF to Editable PDF](actions/pdf-to-editable-pdf.md) | POST | Creates an editable PDF conversion task in ComPDFKit PDF Editor. |
| [PDF to Excel](actions/pdf-to-excel.md) | POST | Creates a PDF-to-Excel conversion task in ComPDFKit PDF Editor. |
| [PDF to HTML](actions/pdf-to-html.md) | POST | Creates a PDF-to-HTML conversion task in ComPDFKit PDF Editor. |
| [PDF to Image](actions/pdf-to-image.md) | POST | Creates a PDF-to-image conversion task in ComPDFKit PDF Editor. |
| [PDF to JSON](actions/pdf-to-json.md) | POST | Creates a PDF-to-JSON conversion task in ComPDFKit PDF Editor. |
| [PDF to Markdown](actions/pdf-to-markdown.md) | POST | Creates a PDF-to-Markdown conversion task in ComPDFKit PDF Editor. |
| [PDF to PPT](actions/pdf-to-ppt.md) | POST | Creates a PDF-to-PPT conversion task in ComPDFKit PDF Editor. |
| [PDF to RTF](actions/pdf-to-rtf.md) | POST | Creates a PDF-to-RTF conversion task in ComPDFKit PDF Editor. |
| [PDF to TXT](actions/pdf-to-txt.md) | POST | Creates a PDF-to-TXT conversion task in ComPDFKit PDF Editor. |
| [PDF to Word](actions/pdf-to-word.md) | POST | Creates a PDF-to-Word conversion task in ComPDFKit PDF Editor. |
| [RTF to PDF](actions/r-tf-to-pdf.md) | POST | Creates an RTF-to-PDF conversion task in ComPDFKit PDF Editor. |
| [RTF to PDF Task](actions/r-tf-to-pdf-task.md) | GET |  |
| [Stamp Detection](actions/stamp-detection.md) | POST | Creates a stamp detection task in ComPDFKit PDF Editor. |
| [TXT to PDF](actions/t-xt-to-pdf.md) | POST | Creates a TXT-to-PDF conversion task in ComPDFKit PDF Editor. |
| [TXT to PDF Task](actions/t-xt-to-pdf-task.md) | GET |  |
| [Table Extraction](actions/table-extraction.md) | POST | Creates a table extraction task in ComPDFKit PDF Editor. |
| [Text Extraction](actions/text-extraction.md) | POST | Creates a text extraction task in ComPDFKit PDF Editor. |
| [Word to PDF](actions/word-to-pdf.md) | POST | Creates a Word-to-PDF conversion task in ComPDFKit PDF Editor. |
| [Word to PDF Task](actions/word-to-pdf-task.md) | GET |  |

