# Update Block with Notion

Updates an existing block in Notion.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/blocks/:block_id`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [Update Block](https://developers.notion.com/reference/update-a-block)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `block_id` | path | `string` | yes | ID of the block to update. |
| `archived` | body | `boolean` | no | Set true to archive this block. |
| `in_trash` | body | `boolean` | no | Set true to move this block to trash. |
