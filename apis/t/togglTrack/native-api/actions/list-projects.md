# List Projects with Toggl Track

Retrieves projects from a Toggl Track workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v9/workspaces/:workspace_id/projects`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [List Projects](https://engineering.toggl.com/docs/track/api/projects/#get-workspaceprojects)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `list<number>` | yes |
| `active` | query | `boolean` | no |
| `since` | query | `number` | no |
| `billable` | query | `boolean` | no |
| `name` | query | `string` | no |
| `search` | query | `string` | no |
| `page` | query | `number` | no |
| `per_page` | query | `number` | no |
| `sort_field` | query | `string` | no |
| `sort_order` | query | `string` | no |
| `only_templates` | query | `boolean` | no |
| `only_me` | query | `boolean` | no |
| `only_editable` | query | `boolean` | no |
| `sort_pinned` | query | `boolean` | no |
