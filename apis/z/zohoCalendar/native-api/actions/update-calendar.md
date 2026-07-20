# Update Calendar with Zoho Calendar

Updates an existing calendar in Zoho Calendar.

## Endpoint

- **Method:** `PUT`
- **Path:** `/calendars/:calendaruid`
- **Base URL:** `https://calendar.zoho.com/api/v1`
- **Official documentation:** [Update Calendar](https://www.zoho.com/calendar/help/api/put-update-calendar.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendaruid` | path | `string` | yes | Calendar unique identifier. |
| `calendarData` | query | `object` | yes | Calendar payload object with the fields to update. |
