# Delete User with Umbrella

Deletes an existing user from Umbrella.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/admin/v2/users/:userId`
- **Base URL:** `https://api.umbrella.com`
- **Official documentation:** [Delete User](https://developer.cisco.com/docs/cloud-security/delete-user/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | no | The Umbrella user ID. |
