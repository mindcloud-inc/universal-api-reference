# <img src="https://images.mindcloud.co/apps/icons/loggly-logo_1776291062579.jpeg" alt="Loggly (Send Data) logo" width="28" height="28"> Loggly (Send Data): Universal API

Send plaintext, JSON, and bulk log events to Loggly over the HTTP/S ingestion endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/logglySendData/latest
- **Category:** IT Operations / Observability
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.loggly.com/
- **Vendor API docs:** https://documentation.solarwinds.com/en/success_center/loggly/content/admin/api-sending-data.htm

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Send Bulk Events](actions/send-bulk-events.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logglySendData/latest/actions/send-bulk-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerToken": "123e4567-e89b-12d3-a456-426614174000",
  "tagPath": "app/server",
  "events": "first event line\\nsecond event line"
}'
```

## Actions (6)

### Log Event

| Action | Method | Description |
| --- | --- | --- |
| [Send Bulk Events](actions/send-bulk-events.md) | POST | Creates bulk log events in Loggly. |
| [Send JSON Event](actions/send-json-event.md) | POST | Creates a JSON log event in Loggly. |
| [Send Multiline Event](actions/send-multiline-event.md) | POST | Creates a multiline log event in Loggly. |
| [Send Plaintext Event](actions/send-plaintext-event.md) | POST | Creates a plain-text log event in Loggly. |
| [Send Tracking Pixel Event](actions/send-tracking-pixel-event.md) | POST | Creates a tracking-pixel log event in Loggly. |
| [Upload Log File](actions/upload-log-file.md) | POST | Uploads a log file to Loggly. |

