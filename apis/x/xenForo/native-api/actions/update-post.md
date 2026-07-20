# Update Post with XenForo

Updates an existing post in XenForo.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/:id/`
- **Base URL:** `{baseUrl}/2310/api`
- **Official documentation:** [Update Post](https://docs.xenforo.com/api/post-posts-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the post to update. |
| `message` | body | `string` | no | Updated post message body. |
| `silent` | body | `boolean` | no | If true and permissions allow, this edit will not show a last edited indication. |
