# <img src="https://images.mindcloud.co/apps/icons/dext_1782742263269.png" alt="Dext logo" width="28" height="28"> Dext: Universal API

Manage clients and monitor document processing activity

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dext/latest
- **Category:** Commerce / Accounting
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.dext.com/
- **Vendor API docs:** https://help.dext.com/en/articles/272702-data-health-insights-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Clients](actions/list-clients.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dext/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Get Client](actions/get-client.md) | GET | Retrieves detailed client information from Dext. |
| [List Clients](actions/list-clients.md) | GET | Retrieves all accessible clients from Dext. |

### Client Activity Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Client Activity Stats](actions/get-client-activity-stats.md) | GET | Retrieves client activity statistics from Dext. |

