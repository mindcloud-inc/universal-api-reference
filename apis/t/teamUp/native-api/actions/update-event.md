# Update Event with TeamUp

Updates an existing event in TeamUp.

## Endpoint

- **Method:** `PUT`
- **Path:** `/:calendarKeyOrId/events/:eventId`
- **Base URL:** `https://api.teamup.com`
- **Official documentation:** [Update Event](https://apidocs.teamup.com/docs/api/8b5d0d1556103-update-an-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The TeamUp event identifier. |
| `start_dt` | body | `string` | yes | Updated event start datetime in TeamUp format. |
| `end_dt` | body | `string` | yes | Updated event end datetime in TeamUp format. |
| `subcalendar_ids[]` | body | `array<number>` | yes | List of TeamUp sub-calendar IDs to assign to the event. |
| `title` | body | `string` | no | Updated event title. |
