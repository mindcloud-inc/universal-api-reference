# Assign Calendar Services with eTermin

Assigns services to a calendar in eTermin.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/calendarservice`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [Assign Calendar Services](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/CalendarService/post_api_calendarservice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendarid` | query | `string` | yes | ID of the calendar |
| `serviceid` | query | `string` | yes | ID of the service |
