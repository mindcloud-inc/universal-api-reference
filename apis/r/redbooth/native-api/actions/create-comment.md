# Create Comment with Redbooth

Creates a new comment in Redbooth.

## Endpoint

- **Method:** `POST`
- **Path:** `/comments`
- **Base URL:** `https://redbooth.com/api/3`
- **Official documentation:** [Create Comment](https://redbooth.com/api/api-docs/#page:comments,header:comments-comment-list-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_id` | body | `number` | yes | Target object ID |
| `target_type` | body | `string` | yes | Target object type |
| `body` | body | `string` | yes | Comment body |
