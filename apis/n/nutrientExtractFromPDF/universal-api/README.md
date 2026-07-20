# <img src="https://images.mindcloud.co/apps/icons/favicon-www-nutrient-io-48x48_1777546859716.png" alt="Nutrient - Extract from PDF logo" width="28" height="28"> Nutrient - Extract from PDF: Universal API

Extract text, structured content, tables, and Markdown from PDF documents using Nutrient DWS Processor API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nutrientExtractFromPDF/latest
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.nutrient.io
- **Vendor API docs:** https://www.nutrient.io/api/extract-text-from-pdf-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Convert PDF to Markdown](actions/convert-pdf-to-markdown.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nutrientExtractFromPDF/latest/actions/convert-pdf-to-markdown?connectionId=$CONNECTION_ID&file=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Pdf Markdown Conversion Result

| Action | Method | Description |
| --- | --- | --- |
| [Convert PDF to Markdown](actions/convert-pdf-to-markdown.md) | GET | Converts a PDF to Markdown with Nutrient. |

### Pdf Plain Text Extraction Result

| Action | Method | Description |
| --- | --- | --- |
| [Extract PDF Plain Text](actions/extract-pdf-plain-text.md) | GET | Extracts plain text from a PDF with Nutrient. |

### Pdf Structured Text Extraction Result

| Action | Method | Description |
| --- | --- | --- |
| [Extract PDF Structured Text](actions/extract-pdf-structured-text.md) | GET | Extracts structured text from a PDF with Nutrient. |

### Pdf Table Extraction Result

| Action | Method | Description |
| --- | --- | --- |
| [Extract PDF Tables as JSON](actions/extract-pdf-tables-as-json.md) | GET | Extracts tables from a PDF as JSON with Nutrient. |

### Pdf Text Extraction Result

| Action | Method | Description |
| --- | --- | --- |
| [Extract PDF Text](actions/extract-pdf-text.md) | GET | Extracts plain and structured text from a PDF with Nutrient. |

