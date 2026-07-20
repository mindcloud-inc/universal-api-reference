# Update Client with Toggl Track

Updates an existing client in Toggl Track.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v9/workspaces/:workspace_id/clients/:client_id`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Update Client](https://engineering.toggl.com/docs/track/api/clients/#put-change-client)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `list<number>` | yes |
| `client_id` | path | `list<number>` | yes |
| `name` | body | `string` | no |
| `notes` | body | `string` | no |
| `external_reference` | body | `string` | no |
