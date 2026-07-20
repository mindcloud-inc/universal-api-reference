# Create Event with Morgen

Creates an event in Morgen.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/events/create`
- **Base URL:** `https://api.morgen.so`
- **Official documentation:** [Create Event](https://docs.morgen.so/events#create-an-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | Calendar account ID. Defaults to the connection accountId. |
| `calendarId` | body | `string` | no | Calendar ID. Defaults to the connection calendarId. |
| `title` | body | `string` | yes | Event title. |
| `start` | body | `string` | yes | LocalDateTime start without timezone offset. |
| `duration` | body | `string` | yes | ISO 8601 duration. |
| `timeZone` | body | `string` | yes | IANA timezone, or null for floating events. |
| `showWithoutTime` | body | `boolean` | yes | Set true for all-day events. |
| `description` | body | `string` | no | Optional event description. |
