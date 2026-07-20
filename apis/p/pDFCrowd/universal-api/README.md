# <img src="https://images.mindcloud.co/apps/icons/pdfcrowd-icon-512_1776182981933.png" alt="PDFCrowd logo" width="28" height="28"> PDFCrowd: Universal API

PDFCrowd converts HTML, images, and PDFs into PDF, image, HTML, or text outputs through a single HTTP conversion API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pDFCrowd/latest
- **Category:** Content & Files / Storage
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pdfcrowd.com/
- **Vendor API docs:** https://pdfcrowd.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Combine PDF Files](actions/combine-pdf-files.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFCrowd/latest/actions/combine-pdf-files" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "f_1": "string",
  "f_2": "string"
}'
```

## Actions (20)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Combine PDF Files](actions/combine-pdf-files.md) | POST | Creates one PDF from multiple PDF files in PDFCrowd. |
| [Convert HTML File to Image](actions/convert-html-file-to-image.md) | POST | Creates an image from an HTML file in PDFCrowd. |
| [Convert HTML File to PDF](actions/convert-html-file-to-pdf.md) | POST | Creates a PDF from an HTML file in PDFCrowd. |
| [Convert HTML String to Image](actions/convert-html-string-to-image.md) | POST | Creates an image from an HTML string in PDFCrowd. |
| [Convert HTML String to PDF](actions/convert-html-string-to-pdf.md) | POST | Creates a PDF from an HTML string in PDFCrowd. |
| [Convert Image File to Image](actions/convert-image-file-to-image.md) | POST | Creates an image from an image file in PDFCrowd. |
| [Convert Image File to PDF](actions/convert-image-file-to-pdf.md) | POST | Creates a PDF from an image file in PDFCrowd. |
| [Convert Image URL to Image](actions/convert-image-url-to-image.md) | POST | Creates an image from an image URL in PDFCrowd. |
| [Convert Image URL to PDF](actions/convert-image-url-to-pdf.md) | POST | Creates a PDF from an image URL in PDFCrowd. |
| [Convert PDF File to HTML](actions/convert-pdf-file-to-html.md) | POST | Creates HTML from a PDF file in PDFCrowd. |
| [Convert PDF File to Image](actions/convert-pdf-file-to-image.md) | POST | Creates an image from a PDF file in PDFCrowd. |
| [Convert PDF File to Text](actions/convert-pdf-file-to-text.md) | POST | Creates text from a PDF file in PDFCrowd. |
| [Convert PDF URL to HTML](actions/convert-pdfurl-to-html.md) | POST | Creates HTML from a PDF URL in PDFCrowd. |
| [Convert PDF URL to Image](actions/convert-pdfurl-to-image.md) | POST | Creates an image from a PDF URL in PDFCrowd. |
| [Convert PDF URL to Text](actions/convert-pdfurl-to-text.md) | POST | Creates text from a PDF URL in PDFCrowd. |
| [Convert URL to Image](actions/convert-url-to-image.md) | POST | Creates an image from a URL in PDFCrowd. |
| [Convert URL to PDF](actions/convert-url-to-pdf.md) | POST | Creates a PDF from a URL in PDFCrowd. |
| [Delete PDF Pages](actions/delete-pdf-pages.md) | POST | Creates a PDF with selected pages deleted in PDFCrowd. |
| [Extract PDF Pages](actions/extract-pdf-pages.md) | POST | Creates a PDF with selected pages extracted in PDFCrowd. |
| [Shuffle PDF Files](actions/shuffle-pdf-files.md) | POST | Creates one PDF by shuffling PDF pages in PDFCrowd. |

