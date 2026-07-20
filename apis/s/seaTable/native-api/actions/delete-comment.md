# Delete Comment with SeaTable

Deletes a comment from a SeaTable base.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api-gateway/api/v2/dtables/:base_uuid/comments/:comment_id/`
- **Base URL:** `https://cloud.seatable.io`
- **Official documentation:** [Delete Comment](https://api.seatable.com/reference/deletecomment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comment_id` | path | `string` | yes | The SeaTable comment ID. |
