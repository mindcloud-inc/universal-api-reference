# Unassign Calendar Services with eTermin

Removes services from a calendar in eTermin.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/calendarservice`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [Unassign Calendar Services](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/CalendarService/delete_api_calendarservice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | ID of the calendar service assignment |
