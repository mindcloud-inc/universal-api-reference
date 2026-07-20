# Create Sales Order with Sage Sales Management

Creates a sales order in Sage Sales Management.

## Endpoint

- **Method:** `POST`
- **Path:** `/salesorders`
- **Base URL:** `https://api.forcemanager.com/api/v4`
- **Official documentation:** [Create Sales Order](https://developer.forcemanager.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `statusId` | body | `string` | yes | Sales order status ID |
