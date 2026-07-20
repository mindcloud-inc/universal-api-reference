# Get Event with TeamUp

Retrieves a single event from TeamUp.

## Endpoint

- **Method:** `GET`
- **Path:** `/:calendarKeyOrId/events/:eventId`
- **Base URL:** `https://api.teamup.com`
- **Official documentation:** [Get Event](https://apidocs.teamup.com/docs/api/016e0077fd9cc-get-an-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The TeamUp event identifier. |
