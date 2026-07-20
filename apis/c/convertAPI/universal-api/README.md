# <img src="https://images.mindcloud.co/apps/icons/convert-api_1782741504157.png" alt="ConvertAPI logo" width="28" height="28"> ConvertAPI: Universal API

ConvertAPI: Convert, extract, compare, watermark, and optimize files

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/convertAPI/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.convertapi.com/
- **Vendor API docs:** https://docs.convertapi.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Add Image Watermark to PDF](actions/add-image-watermark-to-pdf.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/convertAPI/latest/actions/add-image-watermark-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "imageFile": "string"
}'
```

## Actions (30)

### Conversion

| Action | Method | Description |
| --- | --- | --- |
| [Add Image Watermark to PDF](actions/add-image-watermark-to-pdf.md) | POST | Adds an image watermark to a PDF with ConvertAPI. |
| [Add PDF Watermark to PDF](actions/add-pdf-watermark-to-pdf.md) | POST | Adds a PDF watermark to a PDF with ConvertAPI. |
| [Add Text Watermark to PDF](actions/add-text-watermark-to-pdf.md) | POST | Adds a text watermark to a PDF with ConvertAPI. |
| [Compare DOCX Files](actions/compare-docx-files.md) | POST | Compares DOCX files and highlights differences in ConvertAPI. |
| [Compress PDF](actions/compress-pdf.md) | POST | Compresses a PDF to reduce file size in ConvertAPI. |
| [Convert CSV to XLSX](actions/convert-csv-to-xlsx.md) | POST | Converts a CSV file to XLSX with ConvertAPI. |
| [Convert Doc to DOCX](actions/convert-doc-to-docx.md) | POST | Converts a DOC file to DOCX with ConvertAPI. |
| [Convert DOCX to HTML](actions/convert-docx-to-html.md) | POST | Converts a DOCX file to HTML with ConvertAPI. |
| [Convert DOCX to PDF](actions/convert-docx-to-pdf.md) | POST | Converts a DOCX file to PDF with ConvertAPI. |
| [Convert File to PDF](actions/convert-file-to-pdf.md) | POST | Converts a file to PDF with ConvertAPI. |
| [Convert File to Zip](actions/convert-file-to-zip.md) | POST | Converts files to a ZIP archive with ConvertAPI. |
| [Convert HTML to PDF](actions/convert-html-to-pdf.md) | POST | Converts HTML content to PDF with ConvertAPI. |
| [Convert JPG to PDF](actions/convert-jpg-to-pdf.md) | POST | Converts a JPG file to PDF with ConvertAPI. |
| [Convert MSG to PDF](actions/convert-msg-to-pdf.md) | POST | Converts an MSG email to PDF in ConvertAPI. |
| [Convert Office to PDF](actions/convert-office-to-pdf.md) | POST | Converts Word, Excel, or PowerPoint files to PDF in ConvertAPI. |
| [Convert PDF to DOCX](actions/convert-pdf-to-docx.md) | POST | Converts a PDF file to DOCX with ConvertAPI. |
| [Convert PDF to HTML](actions/convert-pdf-to-html.md) | POST | Converts a PDF file to HTML with ConvertAPI. |
| [Convert PDF to JPG](actions/convert-pdf-to-jpg.md) | POST | Converts a PDF file to JPG with ConvertAPI. |
| [Convert PDF to OCR](actions/convert-pdf-to-ocr.md) | POST | Converts a PDF to searchable OCR output in ConvertAPI. |
| [Convert PDF to PDF/A](actions/convert-pdf-to-pdfa.md) | POST | Converts a PDF file to PDF/A with ConvertAPI. |
| [Convert PDF to PNG](actions/convert-pdf-to-png.md) | POST | Converts a PDF file to PNG with ConvertAPI. |
| [Convert PDF to PPTX](actions/convert-pdf-to-pptx.md) | POST | Converts a PDF file to PPTX with ConvertAPI. |
| [Convert PDF to SVG](actions/convert-pdf-to-svg.md) | POST | Converts a PDF file to SVG with ConvertAPI. |
| [Convert PDF to TXT](actions/convert-pdf-to-txt.md) | POST | Converts a PDF file to TXT with ConvertAPI. |
| [Convert PDF to XLSX](actions/convert-pdf-to-xlsx.md) | POST | Converts a PDF file to XLSX with ConvertAPI. |
| [Convert PPTX to PDF](actions/convert-pptx-to-pdf.md) | POST | Converts a PPTX file to PDF with ConvertAPI. |
| [Convert Web to PDF](actions/convert-web-to-pdf.md) | POST | Converts a web page to PDF with ConvertAPI. |
| [Convert XLSX to PDF](actions/convert-xlsx-to-pdf.md) | POST | Converts an XLSX file to PDF with ConvertAPI. |
| [Merge PDF Files](actions/merge-pdf-files.md) | POST | Merges PDF files into one document in ConvertAPI. |
| [Split PDF](actions/split-pdf.md) | POST | Splits a PDF into separate files in ConvertAPI. |

