# List Tags with Toggl Track

Retrieves tags from a Toggl Track workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v9/workspaces/:workspace_id/tags`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [List Tags](https://engineering.toggl.com/docs/track/api/tags/#get-tags)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `list<number>` | yes |
| `page` | query | `number` | no |
| `per_page` | query | `number` | no |
| `search` | query | `string` | no |
