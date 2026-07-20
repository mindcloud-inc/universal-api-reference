# <img src="https://images.mindcloud.co/apps/icons/i-fttt_1776082809544.png" alt="IFTTT logo" width="28" height="28"> IFTTT: Universal API

Manage IFTTT connections and run queries and actions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/iFTTT/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ifttt.com
- **Vendor API docs:** https://ifttt.com/docs/connect_api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Service and User](actions/get-current-service-and-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iFTTT/latest/actions/get-current-service-and-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Service User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Service and User](actions/get-current-service-and-user.md) | GET |  |

