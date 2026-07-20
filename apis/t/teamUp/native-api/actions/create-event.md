# Create Event with TeamUp

Creates a new event in TeamUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/:calendarKeyOrId/events`
- **Base URL:** `https://api.teamup.com`
- **Official documentation:** [Create Event](https://apidocs.teamup.com/docs/api/3269d0159ae9f-create-an-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subcalendar_ids[]` | body | `array<number>` | yes | List of TeamUp sub-calendar IDs to assign to the event. |
| `start_dt` | body | `string` | yes | Event start datetime in TeamUp format. |
| `end_dt` | body | `string` | yes | Event end datetime in TeamUp format. |
| `title` | body | `string` | no | Event title. |
