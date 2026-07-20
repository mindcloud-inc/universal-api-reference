# Cancel Event with Calendly

Cancels a scheduled event in Calendly.

## Endpoint

- **Method:** `POST`
- **Path:** `/scheduled_events/:event_uuid/cancellation`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [Cancel Event](https://developer.calendly.com/api-docs/afb2e9fe3a0a0-cancel-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_uuid` | path | `string` | yes | Scheduled event UUID to cancel. |
| `reason` | body | `string` | no | Cancellation reason. |
