# <img src="https://images.mindcloud.co/apps/icons/h-tml2pdf_1776089539579.png" alt="HTML 2 PDF logo" width="28" height="28"> HTML 2 PDF: Universal API

Generate PDFs from HTML or URLs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hTML2PDF/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://html2pdf.app/
- **Vendor API docs:** https://html2pdf.app/documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Generate PDF](actions/generate-pdf.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hTML2PDF/latest/actions/generate-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "html": "string"
}'
```

## Actions (1)

### Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Generate PDF](actions/generate-pdf.md) | POST |  |

