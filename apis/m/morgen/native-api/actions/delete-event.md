# Delete Event with Morgen

Deletes an event from Morgen.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/events/delete`
- **Base URL:** `https://api.morgen.so`
- **Official documentation:** [Delete Event](https://docs.morgen.so/events#delete-an-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | Calendar account ID. Defaults to the connection accountId. |
| `calendarId` | body | `string` | no | Calendar ID. Defaults to the connection calendarId. |
| `id` | body | `string` | yes | Morgen event ID to delete. |
