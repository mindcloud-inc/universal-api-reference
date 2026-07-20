# List Workspaces with Smartsheet

Retrieves workspaces from Smartsheet.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [List Workspaces](https://developers.smartsheet.com/api/smartsheet/openapi/workspaces/list-workspaces)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `includeAll` | query | `boolean` | no |
| `paginationType` | query | `string` | no |
| `maxItems` | query | `number` | no |
| `lastKey` | query | `string` | no |
