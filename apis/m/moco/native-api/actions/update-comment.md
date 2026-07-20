# Update Comment with Moco

## Endpoint

- **Method:** `PUT`
- **Path:** `/comments/:id`
- **Base URL:** `https://{domain}.mocoapp.com/api/v1`
- **Official documentation:** [Update Comment](https://everii-group.github.io/mocoapp-api-docs/sections/comments.html#put-commentsid)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `attachment_content` | body | `string` | no |
| `attachment_filename` | body | `string` | no |
| `commentable_id` | body | `string` | no |
| `commentable_type` | body | `string` | no |
| `created_at` | body | `string` | no |
| `id` | path | `number` | yes |
| `text` | body | `string` | no |
