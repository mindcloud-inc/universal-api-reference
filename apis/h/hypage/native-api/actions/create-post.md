# Create Post with Hy.page

## Endpoint

- **Method:** `POST`
- **Path:** `/hyax-api/v1/posts`
- **Base URL:** `https://platform.hyax.com`
- **Official documentation:** [Create Post](https://platform.hyax.com/api-docs/post-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | no | Post content. Required for direct mode. |
| `description` | body | `string` | no | Post description. |
| `slug` | body | `string` | no | Post slug. Auto-generated from title if omitted. |
| `status` | body | `string` | no | Post status. |
| `tags` | body | `string` | no | Post tags. |
| `title` | body | `string` | yes | Post title. |
| `generateContent` | body | `boolean` | no | Use AI mode to generate post content. |
