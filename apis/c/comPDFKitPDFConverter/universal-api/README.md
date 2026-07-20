# ComPDFKit PDF Converter: Universal API

Convert PDFs to and from Office, image, text, HTML, CSV, JSON, and Markdown formats with ComPDFKit Cloud conversion APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/comPDFKitPDFConverter/latest
- **Category:** Content & Files / Storage
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.compdf.com/
- **Vendor API docs:** https://api.compdf.com/api-reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Asset Details](actions/get-asset-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/comPDFKitPDFConverter/latest/actions/get-asset-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Get Asset Details](actions/get-asset-details.md) | GET | Retrieves processed asset details from ComPDFKit PDF Converter. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Dewarp Document](actions/dewarp-document.md) | POST | Creates a dewarped document from an uploaded file. |
| [Document Extract](actions/document-extract.md) | POST | Creates document extraction output from an uploaded file. |
| [Layout Analysis](actions/layout-analysis.md) | POST | Creates layout analysis output from a document. |
| [Magic Color](actions/magic-color.md) | POST | Creates a color-enhanced document from an uploaded file. |
| [OCR Document](actions/ocr-document.md) | POST | Creates OCR output from a document file. |
| [Stamp Detection](actions/stamp-detection.md) | POST | Creates stamp detection output from a document. |
| [Table Recognition](actions/table-recognition.md) | POST | Creates table recognition output from a document. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [PDF Compress](actions/pdf-compress.md) | POST | Creates a compressed PDF from an uploaded file. |
| [PDF Content Compare](actions/pdf-content-compare.md) | POST | Creates a content comparison for two PDFs. |
| [PDF Cover Compare](actions/pdf-cover-compare.md) | POST | Creates a cover comparison for two PDFs. |
| [PDF Delete Pages](actions/pdf-delete-pages.md) | POST | Creates a PDF with selected pages deleted. |
| [PDF Extract Pages](actions/pdf-extract-pages.md) | POST | Creates a PDF with selected pages extracted. |
| [PDF Insert Pages](actions/pdf-insert-pages.md) | POST | Creates a PDF with inserted pages. |
| [PDF Merge](actions/pdf-merge.md) | POST | Creates a merged PDF from multiple files. |
| [PDF Rotate Pages](actions/pdf-rotate-pages.md) | POST | Creates a PDF with rotated pages. |
| [PDF Split](actions/pdf-split.md) | POST | Creates split PDF files from a PDF. |
| [PDF to CSV](actions/pdf-to-csv.md) | POST | Creates a CSV file from a PDF. |
| [PDF to DOCX](actions/pdf-to-docx.md) | POST | Creates a DOCX file from a PDF. |
| [PDF to Editable PDF](actions/pdf-to-editable.md) | POST | Creates an editable PDF from a PDF. |
| [PDF to HTML](actions/pdf-to-html.md) | POST | Creates an HTML file from a PDF. |
| [PDF to JPG](actions/pdf-to-jpg.md) | POST | Creates JPG images from a PDF. |
| [PDF to JSON](actions/pdf-to-json.md) | POST | Creates a JSON file from a PDF. |
| [PDF to Markdown](actions/pdf-to-markdown.md) | POST | Creates a Markdown file from a PDF. |
| [PDF to PNG](actions/pdf-to-png.md) | POST | Creates PNG images from a PDF. |
| [PDF to PPTX](actions/pdf-to-pptx.md) | POST | Creates a PPTX file from a PDF. |
| [PDF to RTF](actions/pdf-to-rtf.md) | POST | Creates an RTF file from a PDF. |
| [PDF to TXT](actions/pdf-to-txt.md) | POST | Creates a TXT file from a PDF. |
| [PDF to XLSX](actions/pdf-to-xlsx.md) | POST | Creates an XLSX file from a PDF. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [List Supported PDF Tools](actions/list-supported-pdf-tools.md) | GET | Retrieves supported PDF tools from ComPDFKit PDF Converter. |

