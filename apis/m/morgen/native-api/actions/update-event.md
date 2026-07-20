# Update Event with Morgen

Updates an event in Morgen.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/events/update`
- **Base URL:** `https://api.morgen.so`
- **Official documentation:** [Update Event](https://docs.morgen.so/events#update-an-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | Calendar account ID. Defaults to the connection accountId. |
| `calendarId` | body | `string` | no | Calendar ID. Defaults to the connection calendarId. |
| `id` | body | `string` | yes | Morgen event ID to update. |
| `title` | body | `string` | no | Updated event title. |
| `start` | body | `string` | no | LocalDateTime start without timezone offset. |
| `duration` | body | `string` | no | ISO 8601 duration. Provide with start/timeZone/showWithoutTime when changing timing. |
| `timeZone` | body | `string` | no | IANA timezone. Provide with start/duration/showWithoutTime when changing timing. |
| `showWithoutTime` | body | `boolean` | no | Provide with start/duration/timeZone when changing timing. |
| `description` | body | `string` | no | Updated description. |
