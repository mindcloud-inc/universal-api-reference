# <img src="https://images.mindcloud.co/apps/icons/tik-tok-conversions_1773863943378.png" alt="TikTok Conversions logo" width="28" height="28"> TikTok Conversions: Universal API

Track TikTok conversion events and customer match data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tikTokConversions/latest
- **Category:** Marketing
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://business.tiktok.com/
- **Vendor API docs:** https://business-api.tiktok.com/portal/docs?id=1740963089558529

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Batch Offline Events](actions/batch-offline-events.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/batch-offline-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event_set_id": "string",
  "batch[].event": "string",
  "batch[].timestamp": 1
}'
```

## Actions (14)

### Crm Event Set

| Action | Method | Description |
| --- | --- | --- |
| [Create CRM Event Set](actions/create-crm-event-set.md) | POST |  |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Track Event](actions/track-event.md) | POST | Reports a web event to TikTok Conversions. |

### Offline Event

| Action | Method | Description |
| --- | --- | --- |
| [Batch Offline Events](actions/batch-offline-events.md) | POST | Reports offline events in bulk to TikTok Conversions. |
| [Track Offline Event](actions/track-offline-event.md) | POST | Reports an offline event to TikTok Conversions. |

### Offline Event Set

| Action | Method | Description |
| --- | --- | --- |
| [Create Offline Event Set](actions/create-offline-event-set.md) | POST | Creates a new Offline Event set in TikTok Conversions. |
| [Delete Offline Event Set](actions/delete-offline-event-set.md) | DELETE | Deletes an existing Offline Event set from TikTok Conversions. |
| [Update Offline Event Set](actions/update-offline-event-set.md) | PUT | Updates an existing Offline Event set in TikTok Conversions. |

### Pixel

| Action | Method | Description |
| --- | --- | --- |
| [Create Pixel](actions/create-pixel.md) | POST | Creates a new Pixel in TikTok Conversions. |
| [Update Pixel](actions/update-pixel.md) | PUT | Updates an existing Pixel in TikTok Conversions. |

### Pixel Event

| Action | Method | Description |
| --- | --- | --- |
| [Batch Pixel Events](actions/batch-pixel-events.md) | POST | Tracks Pixel events in bulk in TikTok Conversions. |
| [Create Pixel Event](actions/create-pixel-event.md) | POST | Creates a Pixel event definition in TikTok Conversions. |
| [Delete Pixel Event](actions/delete-pixel-event.md) | DELETE | Deletes an existing Pixel event from TikTok Conversions. |
| [Track Pixel Event](actions/track-pixel-event.md) | POST | Tracks a Pixel event in TikTok Conversions. |
| [Update Pixel Event](actions/update-pixel-event.md) | PUT | Updates a Pixel event definition in TikTok Conversions. |

