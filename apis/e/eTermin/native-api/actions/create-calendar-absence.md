# Create Calendar Absence with eTermin

Creates a new calendar absence in eTermin.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/calendarsnonworkingtimes`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [Create Calendar Absence](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/CalendarsNonWorkingTimes/post_api_calendarsnonworkingtimes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appcalendarid` | query | `number` | yes | ID of the calendar. Use the "Calendar - Get calendar details" function to get a list with all available calendars. |
| `startdate` | query | `string` | yes | Start time of the absence. Format: yyyy-mm-dd HH:MM e.g. 2017-10-24 18:00 |
| `enddate` | query | `string` | yes | End time of the absence. Format: yyyy-mm-dd HH:MM e.g. 2017-10-24 18:00 |
| `reason` | query | `string` | no | Reason or note for the absence. |
| `nwtype` | query | `boolean` | no | Indicates if the absence is dynamic. |
| `dynamicdays` | query | `number` | no | Number of days for the dynamic absence to begin (nwtype has to be 1). |
| `dynamicdaysduration` | query | `number` | no | Number of days for the dynamic absence to last (nwtype has to be 1). |
