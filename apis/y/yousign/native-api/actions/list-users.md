# List Users with Yousign

Retrieves users from Yousign.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://api-sandbox.yousign.app/v3`
- **Official documentation:** [List Users](https://developers.yousign.com/reference/get-users-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Return users after this pagination cursor. |
| `limit` | query | `number` | no | Maximum number of users to return. |
| `email` | query | `string` | no | Filter users by email address. |
