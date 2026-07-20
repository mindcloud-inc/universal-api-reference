# List Available Time Slots with eTermin

Retrieves available time slots from eTermin.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/timeslots`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [List Available Time Slots](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Timeslots/get_api_timeslots)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | yes | Day that you want to check if there are available slots. Format: yyyy-mm-dd |
| `rangesearch` | query | `number` | no | 0 - All slots of a specific day will be displayed <br> 1 - Searches until it found a date when slots are available. Returns the number of slots that are available on a specific day |
| `end` | query | `string` | no | End date of the time range. Only works if rangesearch=1. Format: yyyy-mm-dd |
| `serviceid` | query | `string` | no | ID(s) of the selected service(s). This parameter is required if you restrict the calendar or working times to specific services. Several service ID's can be separated with a comma (,). e.g. 45345,45346 etc. |
| `calendarid` | query | `string` | no | ID of the calendar. Use this parameter if you want to get available time slots for a specific calendar. If this parameter is empty, available time slots for all calendars will be returned. |
| `capacity` | query | `number` | no | Defines the capacity that is searched for, if you have capacity enabled |
| `duration` | query | `number` | no | Appointment duration in minutes. Use this parameter if you want to use a different duration than specified for the service |
| `cluster` | query | `number` | no | Appointment cluster on (1) or off (0) |
