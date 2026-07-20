# Create Event Using Smart Add with Zoho Calendar

Creates a new event in Zoho Calendar using Smart Add.

## Endpoint

- **Method:** `POST`
- **Path:** `/smartadd`
- **Base URL:** `https://calendar.zoho.com/api/v1`
- **Official documentation:** [Create Event Using Smart Add](https://www.zoho.com/calendar/help/api/post-create-event-smart-add.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `saddtext` | query | `string` | yes | Natural-language Smart Add text to turn into an event. Zoho currently expects this query value as saddtext at runtime. |
