# <img src="https://images.mindcloud.co/apps/icons/pi-apiskyreels_1776102664394.png" alt="PiAPI/Skyreels logo" width="28" height="28"> PiAPI/Skyreels: Universal API

Create Skyreels video tasks and get task results

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/piAPISkyreels/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://piapi.ai
- **Vendor API docs:** https://piapi.ai/docs/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPISkyreels/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves information about your PiAPI account. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Skyreels Task](actions/create-skyreels-task.md) | POST | Creates a new Skyreels task in PiAPI. |
| [Get Skyreels Task](actions/get-skyreels-task.md) | GET | Retrieves a Skyreels task by ID from PiAPI. |

