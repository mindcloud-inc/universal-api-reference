# Delete Tag with Toggl Track

Deletes an existing tag from Toggl Track.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v9/workspaces/:workspace_id/tags/:tag_id`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Delete Tag](https://engineering.toggl.com/docs/track/api/tags/#delete-delete-tag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `list<number>` | yes |
| `tag_id` | path | `list<number>` | yes |
