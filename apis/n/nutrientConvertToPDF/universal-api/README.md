# <img src="https://images.mindcloud.co/apps/icons/favicon-www-nutrient-io-48x48_1777546801505.png" alt="Nutrient - Convert to PDF logo" width="28" height="28"> Nutrient - Convert to PDF: Universal API

Convert Office documents, images, HTML, Markdown, URLs, and archival documents into PDF outputs with Nutrient DWS Processor API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nutrientConvertToPDF/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.nutrient.io
- **Vendor API docs:** https://www.nutrient.io/api/pdf-converter-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Convert HTML File to PDF](actions/convert-html-file-to-pdf.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nutrientConvertToPDF/latest/actions/convert-html-file-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

## Actions (6)

### Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Convert HTML File to PDF](actions/convert-html-file-to-pdf.md) | POST | Creates a PDF document from an HTML file in Nutrient. |
| [Convert Image to PDF](actions/convert-image-to-pdf.md) | POST | Creates a PDF document from an image in Nutrient. |
| [Convert Markdown to PDF](actions/convert-markdown-to-pdf.md) | POST | Creates a PDF document from Markdown in Nutrient. |
| [Convert Office Document to PDF](actions/convert-office-document-to-pdf.md) | POST | Creates a PDF document from an Office file in Nutrient. |
| [Convert URL File to PDF](actions/convert-url-file-to-pdf.md) | POST | Creates a PDF document from a file URL in Nutrient. |

### Pdf/a

| Action | Method | Description |
| --- | --- | --- |
| [Convert URL File to PDF/A](actions/convert-url-file-to-pdfa.md) | POST | Creates a PDF/A document from a file URL in Nutrient. |

