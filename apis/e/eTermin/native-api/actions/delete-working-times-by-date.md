# Delete Working Times by Date with eTermin

Deletes working times by date from eTermin.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/workingtimesdate`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [Delete Working Times by Date](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/WorkingTimesDate/delete_api_workingtimesdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendarid` | query | `number` | no | ID of the calendar, every working slot for specific days will be deleted |
| `id` | query | `number` | no | ID of the working time that needs to be deleted |
