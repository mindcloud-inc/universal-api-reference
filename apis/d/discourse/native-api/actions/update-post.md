# Update Post with Discourse

Updates an existing post in Discourse.

## Endpoint

- **Method:** `PUT`
- **Path:** `/posts/:id.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Update Post](https://docs.discourse.org/#tag/Posts/operation/updatePost)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Post id to update. |
| `post.raw` | body | `string` | yes | Updated raw post body. |
| `post.edit_reason` | body | `string` | no | Optional edit reason visible in post history. |
| `bypass_bump` | body | `boolean` | no | Skip bumping the topic when updating the post. |
