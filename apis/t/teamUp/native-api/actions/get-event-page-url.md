# Get Event Page URL with TeamUp

Retrieves the page URL for a TeamUp event.

## Endpoint

- **Method:** `POST`
- **Path:** `/:calendarKey/events/:eventId/pointer`
- **Base URL:** `https://api.teamup.com`
- **Official documentation:** [Get Event Page URL](https://apidocs.teamup.com/docs/api/5d279882e0f60-get-event-page-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The TeamUp event identifier. |
