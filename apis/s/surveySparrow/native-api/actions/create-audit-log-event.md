# Create Audit Log Event with SurveySparrow

Creates a subscribed audit log event in SurveySparrow.

## Endpoint

- **Method:** `POST`
- **Path:** `/audit_logs/events`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [Create Audit Log Event](https://developers.surveysparrow.com/rest-apis/post-v-3-audit-logs-events/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[]` | body | `array<object>` | yes | Array of event objects with name |
| `http_method` | body | `list` | yes | The HTTP method for the request |
| `url` | body | `string` | yes | URL of audit webhook event |
| `headers` | body | `object` | no | Headers object for the webhook request |
