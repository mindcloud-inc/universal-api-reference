# List Content Objects with Flotiq

Retrieves content objects for a Flotiq content type.

## Endpoint

- **Method:** `GET`
- **Path:** `/content/{{name}}`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [List Content Objects](https://flotiq.com/docs/API/content-objects/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The content type name to query. |
