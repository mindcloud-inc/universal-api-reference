# List Spaces with ClickUp

View the Spaces available in a Workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `team/:team_id/space`
- **Base URL:** `https://api.clickup.com/api/v2/`
- **Official documentation:** [List Spaces](https://developer.clickup.com/reference/getspaces)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `boolean` | no | Format: `toggle`. |
| `team_id` | path | `list` | yes | — |
