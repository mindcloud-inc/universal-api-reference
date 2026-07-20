# Get Activity Type with Sage Sales Management

Retrieves an activity type from Sage Sales Management.

## Endpoint

- **Method:** `GET`
- **Path:** `/activityTypes/{{id}}`
- **Base URL:** `https://api.forcemanager.com/api/v4`
- **Official documentation:** [Get Activity Type](https://developer.forcemanager.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Activity type ID |
