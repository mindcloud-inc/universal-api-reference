# List Working Times with eTermin

Retrieves working times from eTermin.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/workingtimes`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [List Working Times](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/WorkingTimes/get_api_workingtimes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendarid` | query | `number` | yes | CalendarID of the calendar you need the working times for |
| `all` | query | `boolean` | no | Use this parameter instead of calendarid, if you want the workingtimes of all calendars |
| `join` | query | `number` | no | Set to 1 for the same information but with names instead of numbers |
