# Update Tag with Toggl Track

Updates an existing tag in Toggl Track.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v9/workspaces/:workspace_id/tags/:tag_id`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Update Tag](https://engineering.toggl.com/docs/track/api/tags/#put-update-tag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `list<number>` | yes |
| `tag_id` | path | `list<number>` | yes |
| `name` | body | `string` | yes |
