# Add Comment to Object with Podio

Creates a comment on a Podio object.

## Endpoint

- **Method:** `POST`
- **Path:** `/comment/:type/:id/`
- **Base URL:** `https://api.podio.com`
- **Official documentation:** [Add Comment to Object](https://developers.podio.com/doc/comments/add-comment-to-object-22340)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `string` | yes | The type of object to comment on. |
| `id` | path | `string` | yes | The ID of the object to comment on. |
| `value` | body | `string` | yes | The comment text to add. |
| `external_id` | body | `string` | no | An external ID for the comment, if any. |
| `file_ids[]` | body | `array<string>` | no | Uploaded file IDs to attach to the comment. |
| `embed_id` | body | `string` | no | The ID of an embedded link created in Podio. |
| `embed_url` | body | `string` | no | A URL to attach to the comment. |
| `alert_invite` | query | `boolean` | no | Automatically invite mentioned users when needed. |
| `hook` | query | `boolean` | no | Run Podio hooks for the change. |
| `silent` | query | `boolean` | no | Suppress stream bumping and notifications for the comment. |
