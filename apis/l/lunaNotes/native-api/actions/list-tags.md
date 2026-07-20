# List Tags with LunaNotes

Retrieves tags from LunaNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/tags`
- **Base URL:** `https://api.lunanotes.io`
- **Official documentation:** [List Tags](https://lunanotes.io/docs/tags/get-v1-tags)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | no | Comma-separated list of related resources to include. |
| `label` | query | `string` | no | Search tags by label using a partial match. |
