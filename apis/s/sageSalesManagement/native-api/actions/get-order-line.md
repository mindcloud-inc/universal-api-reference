# Get Order Line with Sage Sales Management

Retrieves an order line from Sage Sales Management.

## Endpoint

- **Method:** `GET`
- **Path:** `/salesordersLines/{{id}}`
- **Base URL:** `https://api.forcemanager.com/api/v4`
- **Official documentation:** [Get Order Line](https://developer.forcemanager.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Order line ID |
