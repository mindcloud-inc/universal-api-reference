# Share Calendar with Zoho Calendar

Updates calendar sharing in Zoho Calendar.

## Endpoint

- **Method:** `PUT`
- **Path:** `/calendars/:calendaruid/share`
- **Base URL:** `https://calendar.zoho.com/api/v1`
- **Official documentation:** [Share Calendar](https://www.zoho.com/calendar/help/api/put-share-calendar.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendaruid` | path | `string` | yes | Calendar unique identifier. |
| `shareData` | query | `object` | yes | Share payload object describing the permissions to apply. |
