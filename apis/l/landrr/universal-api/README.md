# <img src="https://images.mindcloud.co/apps/icons/landrr-icon_1782393816316.png" alt="Landrr logo" width="28" height="28"> Landrr: Universal API

Build conversational campaigns and review captured leads

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/landrr/latest
- **Category:** Marketing
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://getlandrr.com/
- **Vendor API docs:** https://landrrapp.io/api/documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify API Key](actions/verify-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/landrr/latest/actions/verify-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaign records from Landrr. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Verify API Key](actions/verify-api-key.md) | GET | Retrieves API key verification details from Landrr. |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [List Leads](actions/list-leads.md) | GET | Retrieves lead records from Landrr. |

