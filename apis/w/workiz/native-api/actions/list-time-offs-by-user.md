# List Time Offs by User with Workiz

Finds time off entries in Workiz by user name.

## Endpoint

- **Method:** `GET`
- **Path:** `/TimeOff/get/:USER_NAME`
- **Base URL:** `https://api.workiz.com/api/v1/{apiKey}`
- **Official documentation:** [List Time Offs by User](https://developer.workiz.com/#/Time Off/getUserTimeOff)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `USER_NAME` | path | `string` | yes | The user's name. |
