# List User Hierarchy with Sage Sales Management

Retrieves the user hierarchy from Sage Sales Management.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/{{id}}/hierarchy`
- **Base URL:** `https://api.forcemanager.com/api/v4`
- **Official documentation:** [List User Hierarchy](https://developer.forcemanager.com/)

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
