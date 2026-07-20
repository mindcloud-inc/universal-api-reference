# <img src="https://images.mindcloud.co/apps/icons/com-idp_1776454033430.png" alt="ComIDP logo" width="28" height="28"> ComIDP: Universal API

ComIDP is ComPDF's document processing API for conversion, editing, OCR, and document AI workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/comIDP/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.compdf.com/product/comidp/
- **Vendor API docs:** https://api.compdf.com/api-reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Asset Details](actions/get-asset-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/comIDP/latest/actions/get-asset-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [Get Asset Details](actions/get-asset-details.md) | GET | Retrieves processed asset details from ComIDP. |

### Conversion Job

| Action | Method | Description |
| --- | --- | --- |
| [CSV to PDF](actions/csv-to-pdf.md) | POST | Creates a ComIDP job to convert a CSV file to PDF. |
| [Excel to PDF](actions/excel-to-pdf.md) | POST | Creates a ComIDP job to convert an Excel workbook to PDF. |
| [HTML to PDF](actions/html-to-pdf.md) | POST | Creates a ComIDP job to convert HTML content to PDF. |
| [Image to Excel](actions/image-to-excel.md) | POST | Creates a ComIDP job to convert an image to an Excel workbook. |
| [Image to PPT](actions/image-to-ppt.md) | POST | Creates a ComIDP job to convert an image to PowerPoint. |
| [Image to TXT](actions/image-to-txt.md) | POST | Creates a ComIDP job to convert an image to plain text. |
| [Image to Word](actions/image-to-word.md) | POST | Creates a ComIDP job to convert an image to a Word document. |
| [PDF to CSV](actions/pdf-to-csv.md) | POST | Creates a ComIDP job to convert a PDF to CSV. |
| [PDF to Excel](actions/pdf-to-excel.md) | POST | Creates a ComIDP job to convert a PDF to Excel. |
| [PDF to HTML](actions/pdf-to-html.md) | POST | Creates a ComIDP job to convert a PDF to HTML. |
| [PDF to Image](actions/pdf-to-image.md) | POST | Creates a ComIDP job to convert a PDF to images. |
| [PDF to JSON](actions/pdf-to-json.md) | POST | Creates a ComIDP job to convert a PDF to JSON. |
| [PDF to Markdown](actions/pdf-to-markdown.md) | POST | Creates a ComIDP job to convert a PDF to Markdown. |
| [PDF to PPT](actions/pdf-to-ppt.md) | POST | Creates a ComIDP job to convert a PDF to PowerPoint. |
| [PDF to RTF](actions/pdf-to-rtf.md) | POST | Creates a ComIDP job to convert a PDF to RTF. |
| [PDF to TXT](actions/pdf-to-txt.md) | POST | Creates a ComIDP job to convert a PDF to plain text. |
| [PDF to Word](actions/pdf-to-word.md) | POST | Creates a ComIDP job to convert a PDF to Word. |
| [PNG to PDF](actions/png-to-pdf.md) | POST | Creates a ComIDP job to convert a PNG image to PDF. |
| [PPT to PDF](actions/ppt-to-pdf.md) | POST | Creates a ComIDP job to convert a PowerPoint presentation to PDF. |
| [RTF to PDF](actions/rtf-to-pdf.md) | POST | Creates a ComIDP job to convert an RTF file to PDF. |
| [TXT to PDF](actions/txt-to-pdf.md) | POST | Creates a ComIDP job to convert a text file to PDF. |
| [Word to PDF](actions/word-to-pdf.md) | POST | Creates a ComIDP job to convert a Word document to PDF. |

### Document Extraction Job

| Action | Method | Description |
| --- | --- | --- |
| [Document Extraction](actions/document-extraction.md) | POST | Creates a ComIDP job to extract structured data from documents. |

### Document Parsing Job

| Action | Method | Description |
| --- | --- | --- |
| [Document Parsing](actions/document-parsing.md) | POST | Creates a ComIDP job to parse document content. |

### Image Correction Job

| Action | Method | Description |
| --- | --- | --- |
| [Image Distortion Correction](actions/image-distortion-correction.md) | POST | Creates a ComIDP job to correct image distortion. |

### Image Enhancement Job

| Action | Method | Description |
| --- | --- | --- |
| [Image Enhancement](actions/image-enhancement.md) | POST | Creates a ComIDP job to enhance document images. |

### Stamp Detection Job

| Action | Method | Description |
| --- | --- | --- |
| [Stamp Detection](actions/stamp-detection.md) | POST | Creates a ComIDP job to detect stamps in documents. |

### Table Extraction Job

| Action | Method | Description |
| --- | --- | --- |
| [Table Extraction](actions/table-extraction.md) | POST | Creates a ComIDP job to extract tables from documents. |

### Text Extraction Job

| Action | Method | Description |
| --- | --- | --- |
| [Text Extraction](actions/text-extraction.md) | POST | Creates a ComIDP job to extract text from documents. |

