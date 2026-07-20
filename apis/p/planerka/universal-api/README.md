# <img src="https://images.mindcloud.co/apps/icons/planerka_1776784585921.png" alt="Planerka logo" width="28" height="28"> Planerka: Universal API

Planerka is an online scheduling and booking platform for experts, with meeting types, booking pages, reminders, and event visibility through a small token-authenticated REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/planerka/latest
- **Category:** Productivity / Scheduling
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://planerka.app
- **Vendor API docs:** https://help.planerka.app/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get API status](actions/get-api-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planerka/latest/actions/get-api-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [Get API status](actions/get-api-status.md) | GET | Retrieves API status from Planerka. |

### Calendar Events

| Action | Method | Description |
| --- | --- | --- |
| [List events by date](actions/list-events-by-date.md) | GET | Retrieves events from Planerka for a specific date. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List meeting types](actions/list-meeting-types.md) | GET | Retrieves meeting types from Planerka. |

