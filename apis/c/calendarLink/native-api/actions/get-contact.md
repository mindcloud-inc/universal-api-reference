# Get Contact with CalendarLink

Retrieves a contact from a CalendarLink organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/:organisation/contact/:contact`
- **Base URL:** `https://my.calendarlink.com/api/v1`
- **Official documentation:** [Get Contact](https://api.swaggerhub.com/apis/Calendarlink/calendarlink/1.0.3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact` | path | `string` | yes | CalendarLink contact ID. |
| `organisation` | path | `string` | yes | CalendarLink organization ID. |
