# <img src="https://images.mindcloud.co/apps/icons/event-log-central_1776722240123.png" alt="EventLogCentral logo" width="28" height="28"> EventLogCentral: Universal API

Log, filter, and manage event data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eventLogCentral/latest
- **Category:** IT Operations / Observability
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.eventlogcentral.com
- **Vendor API docs:** https://www.eventlogcentral.com/resources

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Log Event](actions/log-event.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eventLogCentral/latest/actions/log-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string"
}'
```

## Actions (1)

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Log Event](actions/log-event.md) | POST | Creates an event in EventLogCentral. |

