# <img src="https://images.mindcloud.co/apps/icons/sessionize_1778081207608.png" alt="Sessionize logo" width="28" height="28"> Sessionize: Universal API

Read public Sessionize event schedules, sessions, speakers, rooms, categories, and public speaker profile JSON endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sessionize/latest
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sessionize.com
- **Vendor API docs:** https://sessionize.com/playbook/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get All Event Data](actions/get-all-event-data.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sessionize/latest/actions/get-all-event-data?connectionId=$CONNECTION_ID&endpointId=jl4ktls0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Event Data

| Action | Method | Description |
| --- | --- | --- |
| [Get All Event Data](actions/get-all-event-data.md) | GET | Retrieves all event data from Sessionize. |

### Schedule Day

| Action | Method | Description |
| --- | --- | --- |
| [List Schedule Days](actions/list-schedule-days.md) | GET | Retrieves event schedule days from Sessionize. |

### Session Group

| Action | Method | Description |
| --- | --- | --- |
| [List Session Groups](actions/list-session-groups.md) | GET | Retrieves grouped event sessions from Sessionize. |

### Speaker

| Action | Method | Description |
| --- | --- | --- |
| [List Speakers](actions/list-speakers.md) | GET | Retrieves event speaker profiles from Sessionize. |

### Speaker Wall Profile

| Action | Method | Description |
| --- | --- | --- |
| [List Speaker Wall](actions/list-speaker-wall.md) | GET | Retrieves speaker wall profiles from Sessionize. |

