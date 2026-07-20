# Get Client with Toggl Track

Retrieves a client from Toggl Track.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v9/workspaces/:workspace_id/clients/:client_id`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Get Client](https://engineering.toggl.com/docs/track/api/clients/#get-load-client-from-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
| `client_id` | path | `number` | yes |
