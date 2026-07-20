# Update Post with Hy.page

## Endpoint

- **Method:** `PATCH`
- **Path:** `/hyax-api/v1/posts/:id`
- **Base URL:** `https://platform.hyax.com`
- **Official documentation:** [Update Post](https://platform.hyax.com/api-docs/post-patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | no | Updated post content. |
| `id` | path | `string` | yes | Post ID. |
| `slug` | body | `string` | no | Updated post slug. |
| `status` | body | `string` | no | Updated post status. |
| `tags` | body | `string` | no | Updated post tags. |
| `title` | body | `string` | no | Updated post title. |
