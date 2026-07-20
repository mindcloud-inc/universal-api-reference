# List Tags with Systeme.io

Retrieves the collection of tags from Systeme.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/tags`
- **Base URL:** `https://api.systeme.io`
- **Official documentation:** [List Tags](https://developer.systeme.io/reference/api_tags_get_collection-1)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Text search query. |
| `limit` | query | `number` | no | Cursor-based pagination limit (10-100). |
| `startingAfter` | query | `number` | no | Cursor-based pagination starting after this ID. |
| `order` | query | `string` | no | Cursor-based ordering: asc or desc. |
