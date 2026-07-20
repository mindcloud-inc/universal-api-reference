# List Tables with Extruct AI

Retrieves tables from Extruct AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/tables`
- **Base URL:** `https://api.extruct.ai`
- **Official documentation:** [List Tables](https://docs.extruct.ai/api-reference/tables/list-tables)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `kind` | query | `string` | no | Filter by table kind. Accepted values: `0`, `1`, `2`. |
| `scope` | query | `string` | no | Filter by ownership scope. Accepted values: `0`, `1`. |
| `search` | query | `string` | no | Case-insensitive search across table names and descriptions. |
| `tags[]` | query | `array<string>` | no | Repeat this parameter to match tables with any selected tag. |
| `sort` | query | `string` | no | Sort order for returned tables. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
