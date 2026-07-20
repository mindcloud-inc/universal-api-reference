# <img src="https://images.mindcloud.co/apps/icons/morf-1_1777499089126.png" alt="Morf logo" width="28" height="28"> Morf: Universal API

Send patient events and automate healthcare workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/morf/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.morf.health
- **Vendor API docs:** https://www.morf.health/docs/events/payloads/morf/track

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Send Track Event](actions/send-track-event.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/morf/latest/actions/send-track-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event_name": "Ava Chen",
  "user_id": "string"
}'
```

## Actions (1)

### Track Event

| Action | Method | Description |
| --- | --- | --- |
| [Send Track Event](actions/send-track-event.md) | POST | Sends a track event to Morf. |

