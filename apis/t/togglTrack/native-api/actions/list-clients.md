# List Clients with Toggl Track

Retrieves clients from a Toggl Track workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v9/workspaces/:workspace_id/clients`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [List Clients](https://engineering.toggl.com/docs/track/api/clients/#get-list-clients)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `list<number>` | yes |
| `status` | query | `string` | no |
| `name` | query | `string` | no |
