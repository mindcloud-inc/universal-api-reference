# Delete Opportunity with Sage Sales Management

Deletes an opportunity from Sage Sales Management.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/opportunities/{{id}}`
- **Base URL:** `https://api.forcemanager.com/api/v4`
- **Official documentation:** [Delete Opportunity](https://developer.forcemanager.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Opportunity ID |
