# Delete Comment with Lokalise

Deletes a comment from a Lokalise key.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/keys/:key_id/comments/:comment_id`
- **Base URL:** `https://api.lokalise.com/api2`
- **Official documentation:** [Delete Comment](https://developers.lokalise.com/reference/delete-a-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comment_id` | path | `string` | no | Lokalise comment identifier. |
| `key_id` | path | `string` | no | Lokalise key identifier. |
| `project_id` | path | `string` | no | Lokalise project identifier. |
