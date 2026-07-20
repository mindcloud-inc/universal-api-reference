# List Roles of User with Sage Sales Management

Retrieves roles for a user from Sage Sales Management.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/{{id}}/roles`
- **Base URL:** `https://api.forcemanager.com/api/v4`
- **Official documentation:** [List Roles of User](https://developer.forcemanager.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | User ID |
