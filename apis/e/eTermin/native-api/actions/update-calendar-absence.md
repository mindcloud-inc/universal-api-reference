# Update Calendar Absence with eTermin

Updates an existing calendar absence in eTermin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/calendarsnonworkingtimes`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [Update Calendar Absence](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/CalendarsNonWorkingTimes/put_api_calendarsnonworkingtimes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | yes | ID of the absence. |
| `appcalendarid` | query | `number` | no | ID of the calendar. Use the "Calendar - Get calendar details" function to get a list with all available calendars. |
| `startdate` | query | `string` | no | Start time of the absence. Format: yyyy-mm-dd HH:MM e.g. 2017-10-24 18:00 |
| `enddate` | query | `string` | no | End time of the absence. Format: yyyy-mm-dd HH:MM e.g. 2017-10-24 18:00 |
| `reason` | query | `string` | no | Reason or note for the absence. |
| `nwtype` | query | `boolean` | no | Indicates if the absence is dynamic. |
| `dynamicdays` | query | `number` | no | Number of days for the dynamic absence (nwtype has to be 1). |
