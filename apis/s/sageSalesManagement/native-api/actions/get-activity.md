# Get Activity with Sage Sales Management

Retrieves an activity from Sage Sales Management.

## Endpoint

- **Method:** `GET`
- **Path:** `/activities/{{id}}`
- **Base URL:** `https://api.forcemanager.com/api/v4`
- **Official documentation:** [Get Activity](https://developer.forcemanager.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Activity ID |
