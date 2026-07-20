# Search calendars with AddEvent

## Endpoint

- **Method:** `GET`
- **Path:** `/calendars`
- **Base URL:** `https://api.addevent.com/calevent/v2`
- **Official documentation:** [Search calendars](https://docs.addevent.com/reference/search-calendars)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendar_ids[]` | query | `array<string>` | no | Comma-separated list of calendar IDs. Limits search results to those specific calendars. Send multiple values as a string separated by `,`. |
