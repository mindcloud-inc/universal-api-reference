# Create One-Off Event Type with Calendly

Creates a one-off event type in Calendly.

## Endpoint

- **Method:** `POST`
- **Path:** `/one_off_event_types`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [Create One-Off Event Type](https://developer.calendly.com/api-docs/v1yuxil3cpmxq-create-one-off-event-type)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | One-off event type name. |
| `host` | body | `string` | yes | Host URI (user URI). |
| `duration` | body | `number` | yes | Duration in minutes. |
| `timezone` | body | `string` | no | Event timezone. |
| `date_setting` | body | `object` | yes | — |
| `date_setting.type` | body | `string` | yes | Date setting type for one-off event type. |
| `date_setting.start_date` | body | `date` | yes | Date value when using a specific day. |
| `date_setting.end_date` | body | `date` | yes | Date range end date (YYYY-MM-DD). |
