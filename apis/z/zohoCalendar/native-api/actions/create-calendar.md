# Create Calendar with Zoho Calendar

Creates a new personal calendar in Zoho Calendar.

## Endpoint

- **Method:** `POST`
- **Path:** `/calendars`
- **Base URL:** `https://calendar.zoho.com/api/v1`
- **Official documentation:** [Create Calendar](https://www.zoho.com/calendar/help/api/post-create-calendar.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendarData` | query | `object` | yes | Calendar payload object describing the calendar to create. |
