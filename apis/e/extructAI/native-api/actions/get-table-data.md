# Get Table Data with Extruct AI

Retrieves table data from Extruct AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/tables/:table_id/data`
- **Base URL:** `https://api.extruct.ai`
- **Official documentation:** [Get Table Data](https://docs.extruct.ai/api-reference/tables/get-table-data)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `string` | yes | Target table identifier. |
