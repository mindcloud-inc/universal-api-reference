# <img src="https://images.mindcloud.co/apps/icons/unnamed_1780948582417.png" alt="AppFit logo" width="28" height="28"> AppFit: Universal API

Track product metrics, share reports, and log product changes

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/appFit/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.appfit.io
- **Vendor API docs:** https://www.appfit.io/documentation/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Track Metric Event](actions/track-metric-event.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appFit/latest/actions/track-metric-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "occurredAt": "2026-05-07T12:00:00.000Z",
  "payload": {}
}'
```

## Actions (2)

### Metric Event

| Action | Method | Description |
| --- | --- | --- |
| [Track Metric Event](actions/track-metric-event.md) | POST | Creates a metric event in AppFit. |

### Metric Event Batch

| Action | Method | Description |
| --- | --- | --- |
| [Track Metric Event Batch](actions/track-metric-event-batch.md) | POST | Creates a batch of metric events in AppFit. |

