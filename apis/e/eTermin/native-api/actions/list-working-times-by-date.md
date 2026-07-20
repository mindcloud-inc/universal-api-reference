# List Working Times by Date with eTermin

Retrieves working times by date from eTermin.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/workingtimesdate`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [List Working Times by Date](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/WorkingTimesDate/get_api_workingtimesdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendarid` | query | `number` | yes | CalendarID of the calendar you need the working times for |
| `join` | query | `number` | no | Set to 1 for the same information but with names instead of numbers |
| `start` | query | `string` | no | Start date from when the workingtimes should be shown. Format needs to be yyyy-mm-dd |
| `end` | query | `string` | no | End date until the workingtimes should be shown. Needs the start parameter. Format needs to be yyyy-mm-dd |
