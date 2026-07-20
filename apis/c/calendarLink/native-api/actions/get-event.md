# Get Event with CalendarLink

Retrieves an event from a CalendarLink organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/:organisation/event/:event`
- **Base URL:** `https://my.calendarlink.com/api/v1`
- **Official documentation:** [Get Event](https://api.swaggerhub.com/apis/Calendarlink/calendarlink/1.0.3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | path | `string` | yes | CalendarLink event ID. |
| `organisation` | path | `string` | yes | CalendarLink organization ID. |
