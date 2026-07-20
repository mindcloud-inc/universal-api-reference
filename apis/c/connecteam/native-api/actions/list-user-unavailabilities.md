# List User Unavailabilities with Connecteam

Retrieve a list of user unavailabilities, approved time-off requests and assigned shifts

## Endpoint

- **Method:** `GET`
- **Path:** `/scheduler/v1/schedulers/user-unavailability`
- **Base URL:** `https://api.connecteam.com`
- **Official documentation:** [List User Unavailabilities](https://developer.connecteam.com/reference/get_unavailabilities_scheduler_v1_schedulers_user_unavailability_get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `userId` | query | `number` | yes |
| `startTime` | query | `number` | yes |
| `endTime` | query | `number` | yes |
