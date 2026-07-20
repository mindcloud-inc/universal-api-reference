# <img src="https://images.mindcloud.co/apps/icons/sales-viewer_1773856250050.png" alt="SalesViewer logo" width="28" height="28"> SalesViewer: Universal API

SalesViewer is a website visitor intelligence platform that exposes a compact REST API for querying tracked visitor sessions and related website activity.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/salesViewer/latest
- **Category:** Marketing
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.salesviewer.com/
- **Vendor API docs:** https://salesviewer.github.io/salesviewer-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Sessions](actions/search-sessions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesViewer/latest/actions/search-sessions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Search Sessions](actions/search-sessions.md) | GET | Finds sessions in SalesViewer by query parameters. |
| [Search Sessions by Form Data](actions/search-sessions-by-form-data.md) | GET | Finds sessions in SalesViewer by form data. |

