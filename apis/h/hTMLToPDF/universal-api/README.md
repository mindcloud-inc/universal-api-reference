# <img src="https://images.mindcloud.co/apps/icons/icon_1781898994556.png" alt="HTML to PDF logo" width="28" height="28"> HTML to PDF: Universal API

Convert HTML content or a public URL into PDF documents with the official HTML to PDF API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hTMLToPDF/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.htmltopdfapi.co/
- **Vendor API docs:** https://platform.htmltopdfapi.co/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate API Key](actions/validate-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hTMLToPDF/latest/actions/validate-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Validate API Key](actions/validate-api-key.md) | GET |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Generate PDF from HTML](actions/generate-pdf-from-html.md) | POST |  |
| [Generate PDF from URL](actions/generate-pdf-from-url.md) | POST |  |

