# Search Content with Flotiq

Searches content objects across your Flotiq project.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [Search Content](https://flotiq.com/docs/API/search/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | The search query string. |
| `content_type[]` | query | `string` | no | Optional content type name to scope search results. |
