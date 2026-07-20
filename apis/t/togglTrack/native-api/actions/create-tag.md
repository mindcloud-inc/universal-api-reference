# Create Tag with Toggl Track

Creates a new tag in Toggl Track.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v9/workspaces/:workspace_id/tags`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Create Tag](https://engineering.toggl.com/docs/track/api/tags/#post-create-tag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `list<number>` | yes |
| `name` | body | `string` | yes |
