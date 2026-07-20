# List Event Registrations with CalendarLink

Retrieves event registrations from a CalendarLink event.

## Endpoint

- **Method:** `GET`
- **Path:** `/:organisation/event/:event/registration`
- **Base URL:** `https://my.calendarlink.com/api/v1`
- **Official documentation:** [List Event Registrations](https://api.swaggerhub.com/apis/Calendarlink/calendarlink/1.0.3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | path | `string` | yes | CalendarLink event ID. |
| `organisation` | path | `string` | yes | CalendarLink organization ID. |
