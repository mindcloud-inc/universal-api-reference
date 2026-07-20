# Update Tag with Teyuto

Updates an existing tag in Teyuto.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tags/:tag_id`
- **Base URL:** `https://api.teyuto.tv/v2`
- **Official documentation:** [Update Tag](https://docs.teyuto.com/api/edit-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag_id` | path | `string` | yes | The Teyuto tag ID to update. |
| `title` | body | `string` | yes | Updated title of the tag. |
| `hidden` | body | `boolean` | yes | Whether the tag should be hidden. |
