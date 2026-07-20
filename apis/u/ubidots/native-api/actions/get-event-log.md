# Get Event Log with Ubidots

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:event_key/logs/:log_id/`
- **Base URL:** `https://industrial.api.ubidots.com/api/v2.0`
- **Official documentation:** [Get Event Log](https://docs.ubidots.com/reference/get-event-log)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_key` | path | `string` | yes | The event ID or key. |
| `log_id` | path | `string` | yes | The event log ID. |
