# Search events with AddEvent

## Endpoint

- **Method:** `GET`
- **Path:** `/events`
- **Base URL:** `https://api.addevent.com/calevent/v2`
- **Official documentation:** [Search events](https://docs.addevent.com/reference/search-events)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendar_ids[]` | query | `array<string>` | no | Comma-separated list of calendar IDs. Limits search results to those specific calendars. Send multiple values as a string separated by `,`. |
| `event_ids[]` | query | `array<string>` | no | Comma-separated list of event IDs. Limits search results to those specific events. Send multiple values as a string separated by `,`. |
| `datetime_min` | query | `string` | no | Limits search results to events that end after this time. |
| `datetime_max` | query | `string` | no | Limits search results to events that start before this time. |
| `search` | query | `string` | no | Search term applied across event title, internal name, description, and location. |
| `custom_data_key` | query | `string` | no | Custom data key to pair with Custom Data Value when filtering results. |
| `custom_data_value` | query | `string` | no | Custom data value to pair with Custom Data Key when filtering results. |
