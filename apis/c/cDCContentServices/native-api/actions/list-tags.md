# List Tags with CDC Content Services

Retrieves tags from CDC Content Services.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/resources/tags`
- **Base URL:** `https://tools.cdc.gov/api`
- **Official documentation:** [List Tags](https://tools.cdc.gov/api/docs/info.aspx)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nameContains` | query | `string` | no | Return tags whose name contains this value. |
| `language` | query | `string` | no | Filter tags by language. |
| `mediaId` | query | `number` | no | Return tags associated with the supplied media id. |
| `typeName` | query | `string` | no | Return tags belonging to the supplied tag type name. |
