# List Block Children with Notion

Retrieves child blocks for a Notion block.

## Endpoint

- **Method:** `GET`
- **Path:** `/blocks/:block_id/children`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [List Block Children](https://developers.notion.com/reference/get-block-children)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `block_id` | path | `string` | yes | ID of the parent block. |
| `page_size` | query | `number` | no | Maximum number of children to return (max 100). |
| `start_cursor` | query | `string` | no | Cursor from a previous response to continue pagination. |
