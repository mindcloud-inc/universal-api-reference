# Create Client with Toggl Track

Creates a new client in Toggl Track.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v9/workspaces/:workspace_id/clients`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Create Client](https://engineering.toggl.com/docs/track/api/clients/#post-create-client)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `list<number>` | yes |
| `name` | body | `string` | yes |
| `notes` | body | `string` | no |
