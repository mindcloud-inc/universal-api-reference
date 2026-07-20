# Get Workspace Users with Toggl Track

Retrieves workspace users from Toggl Track.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v9/workspaces/:workspace_id/users`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Get Workspace Users](https://engineering.toggl.com/docs/track/api/workspaces/#get-get-workspace-users)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `list<number>` | yes |
| `exclude_deleted` | query | `boolean` | no |
