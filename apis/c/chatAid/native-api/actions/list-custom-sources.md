# List Custom Sources with Chat Aid

Retrieves custom sources from your Chat Aid workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/external/sources/custom`
- **Base URL:** `https://api.chataid.com`
- **Official documentation:** [List Custom Sources](https://docs.chataid.com/api-guide/custom-sources)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter sources by partial, case-insensitive name. |
| `status` | query | `list` | no | Filter sources by status. Accepted values: `Active`, `Error`, `Processing`. |
| `type` | query | `string` | no | Filter sources by file type. |
| `teamId` | query | `string` | no | Filter sources by team ID. |
