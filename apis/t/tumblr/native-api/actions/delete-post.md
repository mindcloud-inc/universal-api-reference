# Delete Post with Tumblr

Deletes an existing post from Tumblr.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/blog/:blogIdentifier/post/delete`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [Delete Post](https://www.tumblr.com/docs/en/api/v2#postdelete--delete-a-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blogIdentifier` | path | `string` | yes | Any Tumblr blog identifier for the target blog. |
| `id` | body | `string` | yes | ID of the post to delete. |
