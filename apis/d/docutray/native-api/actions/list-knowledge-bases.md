# List Knowledge Bases with Docutray

## Endpoint

- **Method:** `GET`
- **Path:** `api/knowledge-bases`
- **Base URL:** `https://app.docutray.com`
- **Official documentation:** [List Knowledge Bases](https://docs.docutray.com/docs/operations/knowledge-bases)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isActive` | query | `boolean` | no | Filter by active status |
| `search` | query | `string` | no | Search by name or description |
