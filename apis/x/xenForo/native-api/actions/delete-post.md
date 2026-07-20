# Delete Post with XenForo

Deletes an existing post from XenForo.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/posts/:id/`
- **Base URL:** `{baseUrl}/2310/api`
- **Official documentation:** [Delete Post](https://docs.xenforo.com/api/delete-posts-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the post to delete. |
| `hard_delete` | query | `boolean` | no | If true, permanently delete the post instead of soft deleting it. |
| `reason` | query | `string` | no | Reason shown for a soft deletion. |
