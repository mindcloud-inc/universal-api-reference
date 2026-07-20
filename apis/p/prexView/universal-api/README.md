# <img src="https://images.mindcloud.co/apps/icons/prex-view_1778174000602.png" alt="PrexView logo" width="28" height="28"> PrexView: Universal API

Transform XML or JSON into PDFs, HTML, PNGs, or JPGs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/prexView/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://prexview.com
- **Vendor API docs:** https://prexview.com/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Create document from JSON](actions/create-document-from-json.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prexView/latest/actions/create-document-from-json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "json": "Paste JSON data",
  "template": "invoice-customer-{{Data.customer}}",
  "output": "pdf"
}'
```

## Actions (2)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create document from JSON](actions/create-document-from-json.md) | POST | Creates a document in PrexView from JSON data. |
| [Create document from XML](actions/create-document-from-xml.md) | POST | Creates a document in PrexView from XML data. |

