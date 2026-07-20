# List Users with Userflow

Retrieves a list of users from Userflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://api.userflow.com`
- **Official documentation:** [List Users](https://docs.userflow.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of users to return. |
| `starting_after` | query | `string` | no | Return users after this user ID. |
| `order_by` | query | `string` | no | Sort users by one or more supported fields. |
