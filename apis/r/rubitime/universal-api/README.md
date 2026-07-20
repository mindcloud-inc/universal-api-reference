# <img src="https://images.mindcloud.co/apps/icons/rubitime_1776802593786.png" alt="Rubitime logo" width="28" height="28"> Rubitime: Universal API

Rubitime is an online appointment scheduling and booking service for service businesses. Its API supports managing appointment records and checking available booking times.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rubitime/latest
- **Category:** Productivity / Scheduling
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rubitime.ru/
- **Vendor API docs:** https://rubitime.ru/faq/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Record](actions/get-record.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rubitime/latest/actions/get-record?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | POST | Creates a new record in Rubitime. |
| [Get Record](actions/get-record.md) | GET | Retrieves a record from Rubitime. |
| [Remove Record](actions/remove-record.md) | DELETE | Deletes an existing record from Rubitime. |
| [Update Record](actions/update-record.md) | PUT | Updates an existing record in Rubitime. |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Get Schedule](actions/get-schedule.md) | GET | Retrieves booking dates and times from Rubitime. |

