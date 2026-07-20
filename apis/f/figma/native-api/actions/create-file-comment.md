# Create File Comment with Figma

Creates a new comment in a Figma file.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/:file_key/comments`
- **Base URL:** `https://api.figma.com/v1`
- **Official documentation:** [Create File Comment](https://developers.figma.com/docs/rest-api/comments-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_key` | path | `string` | yes | Key of the Figma file. |
| `message` | body | `string` | yes | Comment text content. |
| `comment_id` | body | `string` | no | Parent comment ID to create a reply thread. |
| `client_meta` | body | `object` | no | Position metadata for where to place the comment. |
