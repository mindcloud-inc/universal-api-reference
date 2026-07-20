# Get User Duty Status with SIGNL4

Retrieves a user's duty status from SIGNL4.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/users/{userId}/dutyStatus`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Get User Duty Status](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | Identifier of the user to get. Use 'Me' to get information about the currently logged in user. This is not possible with an api key. Can also be an email address of a user in the team or the unique id of an according user object.” |
| `teamId[]` | query | `array<string>` | no | — |
