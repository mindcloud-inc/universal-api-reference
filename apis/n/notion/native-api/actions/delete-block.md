# Delete Block with Notion

Deletes an existing block from Notion.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/blocks/:block_id`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [Delete Block](https://developers.notion.com/reference/delete-a-block)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `block_id` | path | `string` | yes | ID of the block to delete. |
