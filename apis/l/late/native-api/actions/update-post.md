# Update Post with Late

## Endpoint

- **Method:** `PUT`
- **Path:** `/posts/:postId`
- **Base URL:** `https://zernio.com/api/v1`
- **Official documentation:** [Update Post](https://docs.zernio.com/posts/update-post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `postId` | path | `string` | yes |
| `content` | body | `string` | no |
| `scheduledFor` | body | `string` | no |
| `tiktokSettings` | body | `object` | no |
| `recycling` | body | `object` | no |
