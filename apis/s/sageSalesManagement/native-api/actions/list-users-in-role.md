# List Users in Role with Sage Sales Management

Retrieves users in a role from Sage Sales Management.

## Endpoint

- **Method:** `GET`
- **Path:** `/roles/{{id}}/users`
- **Base URL:** `https://api.forcemanager.com/api/v4`
- **Official documentation:** [List Users in Role](https://developer.forcemanager.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Role ID |
