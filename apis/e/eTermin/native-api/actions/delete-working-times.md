# Delete Working Times with eTermin

Deletes existing working times from eTermin.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/workingtimes`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [Delete Working Times](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/WorkingTimes/delete_api_workingtimes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendarid` | query | `number` | yes | ID of the calendar |
| `id` | query | `number` | no | ID of the working time that needs to be deleted. If not provided, every working slot of the calendar will be deleted |
