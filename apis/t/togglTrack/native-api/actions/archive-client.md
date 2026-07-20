# Archive Client with Toggl Track

Archives an existing client in Toggl Track.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v9/workspaces/:workspace_id/clients/:client_id/archive`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Archive Client](https://engineering.toggl.com/docs/track/api/clients/#post-archives-client)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
| `client_id` | path | `number` | yes |
