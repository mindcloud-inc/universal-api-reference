# Append Block Children with Notion

Appends child blocks to a Notion block.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/blocks/:block_id/children`
- **Base URL:** `https://api.notion.com/v1`
- **Official documentation:** [Append Block Children](https://developers.notion.com/reference/patch-block-children)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `block_id` | path | `string` | yes | ID of the parent block where children are appended. |
| `children` | body | `list<object>` | yes | Array of block objects to append as children. |
| `position` | body | `object` | no | Optional insertion position object for append operations. |
| `after` | body | `string` | no | Deprecated: ID of existing child block to append after. |
