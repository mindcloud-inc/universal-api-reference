# Search calendar subscribers with AddEvent

## Endpoint

- **Method:** `GET`
- **Path:** `/subscribers`
- **Base URL:** `https://api.addevent.com/calevent/v2`
- **Official documentation:** [Search calendar subscribers](https://docs.addevent.com/reference/search-calendar-subscribers)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendar_ids[]` | query | `array<string>` | no | Limit results to specific calendars. Send multiple values as a string separated by `,`. |
