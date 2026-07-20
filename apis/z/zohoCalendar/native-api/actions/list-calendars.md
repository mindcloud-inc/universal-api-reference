# List Calendars with Zoho Calendar

Retrieves user calendars from Zoho Calendar.

## Endpoint

- **Method:** `GET`
- **Path:** `/calendars`
- **Base URL:** `https://calendar.zoho.com/api/v1`
- **Official documentation:** [List Calendars](https://www.zoho.com/calendar/help/api/get-calendar-list.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Category` | query | `string` | no | Filter calendars by category: own, group, app, others, or all. |
