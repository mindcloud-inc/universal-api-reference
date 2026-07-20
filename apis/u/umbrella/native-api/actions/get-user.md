# Get User with Umbrella

Retrieves user account details from Umbrella.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/v2/users/:userId`
- **Base URL:** `https://api.umbrella.com`
- **Official documentation:** [Get User](https://developer.cisco.com/docs/cloud-security/get-user/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | no | The Umbrella user ID. |
