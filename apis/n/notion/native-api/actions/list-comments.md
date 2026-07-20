# List Comments with Notion

Retrieves comments from the connected Notion workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/comments`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [List Comments](https://developers.notion.com/reference/list-comments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `block_id` | query | `string` | yes | ID of the page or block to list comments for. |
| `start_cursor` | query | `string` | no | Cursor for pagination. |
| `page_size` | query | `number` | no | Maximum number of comments per page (max 100). |
