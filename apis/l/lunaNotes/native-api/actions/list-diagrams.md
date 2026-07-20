# List Diagrams with LunaNotes

Retrieves diagrams from LunaNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/diagrams`
- **Base URL:** `https://api.lunanotes.io`
- **Official documentation:** [List Diagrams](https://lunanotes.io/docs/diagrams/get-v1-diagrams)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | no | Comma-separated list of related resources to include. |
| `type` | query | `string` | no | Filter by diagram type. |
| `videoId` | query | `string` | no | Filter by video ID. |
