# <img src="https://images.mindcloud.co/apps/icons/images-9_1774539593899.png" alt="Syften logo" width="28" height="28"> Syften: Universal API

Monitor web mentions and manage keyword alerts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/syften/latest
- **Category:** Marketing
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://syften.com
- **Vendor API docs:** https://github.com/syften/syften-examples

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Info](actions/get-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syften/latest/actions/get-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Info](actions/get-info.md) | GET | Retrieves account details and plan information from Syften. |

### Filter

| Action | Method | Description |
| --- | --- | --- |
| [List Filters](actions/list-filters.md) | GET | Retrieves saved keyword filters from Syften. |
| [Set Filters](actions/set-filters.md) | PUT | Updates the saved filter list in Syften. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [List Items](actions/list-items.md) | GET | Retrieves matching mention items from Syften. |

### Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Settings](actions/get-settings.md) | GET | Retrieves keyword alert settings from Syften. |

