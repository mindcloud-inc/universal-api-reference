# List Calendars with eTermin

Retrieves calendars from eTermin.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/calendar`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [List Calendars](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Calendar/get_api_calendar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendarid` | query | `number` | no | ID of the calendar, if you only need to get the details of a single calendar |
