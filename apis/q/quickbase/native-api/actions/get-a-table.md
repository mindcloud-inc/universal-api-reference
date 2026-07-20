# Get a Table with Quickbase

Retrieves a Quickbase table by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/tables/:tableId`
- **Base URL:** `https://api.quickbase.com`
- **Official documentation:** [Get a Table](https://developer.quickbase.com/operation/getTable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | query | `string` | yes | The Quickbase app identifier. |
| `tableId` | path | `string` | yes | The Quickbase table identifier. |
