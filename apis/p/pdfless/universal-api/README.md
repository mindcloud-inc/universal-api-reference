# <img src="https://images.mindcloud.co/apps/icons/pdfless_1774973919859.png" alt="Pdfless logo" width="28" height="28"> Pdfless: Universal API

Generate PDFs from templates and JSON data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pdfless/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pdfless.com/
- **Vendor API docs:** https://docs.pdfless.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Generate PDF](actions/generate-pdf.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pdfless/latest/actions/generate-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

## Actions (1)

### Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Generate PDF](actions/generate-pdf.md) | POST |  |

