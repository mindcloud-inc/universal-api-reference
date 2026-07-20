# Get Sales Order with Sage Sales Management

Retrieves a sales order from Sage Sales Management.

## Endpoint

- **Method:** `GET`
- **Path:** `/salesorders/{{id}}`
- **Base URL:** `https://api.forcemanager.com/api/v4`
- **Official documentation:** [Get Sales Order](https://developer.forcemanager.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Sales order ID |
