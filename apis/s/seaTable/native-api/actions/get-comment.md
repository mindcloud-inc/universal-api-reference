# Get Comment with SeaTable

Retrieves a comment from a SeaTable base.

## Endpoint

- **Method:** `GET`
- **Path:** `/api-gateway/api/v2/dtables/:base_uuid/comments/:comment_id/`
- **Base URL:** `https://cloud.seatable.io`
- **Official documentation:** [Get Comment](https://api.seatable.com/reference/getcomment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comment_id` | path | `string` | yes | The SeaTable comment ID. |
