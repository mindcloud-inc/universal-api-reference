# Post Event with Datadog

Creates a new event in Datadog.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/events`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [Post Event](https://docs.datadoghq.com/api/latest/events/#post-an-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Title of the event. |
| `text` | body | `string` | yes | Body text for the event. |
| `aggregation_key` | body | `string` | no | Aggregation key for grouping events. |
| `alert_type` | body | `string` | no | Alert type for the event. |
| `date_happened` | body | `number` | no | POSIX timestamp of the event. |
| `device_name` | body | `string` | no | Device name to associate with the event. |
| `host` | body | `string` | no | Host name associated with the event. |
| `priority` | body | `string` | no | Priority of the event. |
| `related_event_id` | body | `number` | no | Related event identifier. |
| `source_type_name` | body | `string` | no | Source type name for the event. |
| `tags[]` | body | `array<string>` | no | Tags to attach to the event. |
