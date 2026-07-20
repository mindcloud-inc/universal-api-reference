# <img src="https://images.mindcloud.co/apps/icons/a-itextraction_1774297336082.png" alt="AI Textraction logo" width="28" height="28"> AI Textraction: Universal API

Extract custom user-defined entities from unstructured text with AI-powered parsing.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aITextraction/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.textraction.ai/
- **Vendor API docs:** https://rapidapi.com/textractionai/api/ai-textraction/details

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Extract Data](actions/extract-data.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aITextraction/latest/actions/extract-data?connectionId=$CONNECTION_ID&text=string&entities=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Extract Data](actions/extract-data.md) | GET | Extracts user-defined entities from unstructured text with AI Textraction. |

