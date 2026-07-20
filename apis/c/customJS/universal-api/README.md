# <img src="https://images.mindcloud.co/apps/icons/custom-js_1774978690245.png" alt="CustomJS logo" width="28" height="28"> CustomJS: Universal API

Generate PDFs, capture screenshots, scrape websites, and execute JavaScript

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/customJS/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.customjs.space/products/pdf-generation/
- **Vendor API docs:** https://www.customjs.space/integration/native-api/documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List HTML Pages](actions/list-html-pages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customJS/latest/actions/list-html-pages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Convert PDF to Text](actions/convert-pdf-to-text.md) | GET | Extracts text from a PDF in CustomJS. |
| [Execute Custom JavaScript](actions/execute-custom-java-script.md) | GET | Executes custom JavaScript code in CustomJS. |
| [List HTML Pages](actions/list-html-pages.md) | GET | Retrieves hosted HTML pages from CustomJS. |
| [Scrape HTML](actions/scrape-html.md) | GET | Retrieves HTML content from a website using CustomJS. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Capture Screenshot](actions/capture-screenshot.md) | POST | Captures a website screenshot in CustomJS. |
| [Compress PDF](actions/compress-pdf.md) | POST | Compresses a PDF in CustomJS. |
| [Convert HTML to PDF](actions/convert-html-to-pdf.md) | POST | Converts HTML to a PDF in CustomJS. |
| [Convert HTML to PNG](actions/convert-html-to-png.md) | POST | Converts HTML to a PNG in CustomJS. |
| [Convert Markdown to PDF](actions/convert-markdown-to-pdf.md) | POST | Converts Markdown to a PDF in CustomJS. |
| [Convert PDF to PNG](actions/convert-pdf-to-png.md) | POST | Converts a PDF to PNG images in CustomJS. |
| [Extract Pages from PDF](actions/extract-pages-from-pdf.md) | POST | Extracts selected pages from a PDF in CustomJS. |
| [Merge PDFs](actions/merge-pdfs.md) | POST | Merges PDF files into one PDF in CustomJS. |

