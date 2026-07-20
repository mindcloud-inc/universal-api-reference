# Delete Event with TeamUp

Deletes an existing event from TeamUp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/:calendarKeyOrId/events/:eventId`
- **Base URL:** `https://api.teamup.com`
- **Official documentation:** [Delete Event](https://apidocs.teamup.com/docs/api/260f3631bec7b-delete-an-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The TeamUp event identifier. |
