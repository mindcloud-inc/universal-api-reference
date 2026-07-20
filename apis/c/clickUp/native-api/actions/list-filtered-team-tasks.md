# List Filtered Team Tasks with ClickUp

View the tasks that meet specific criteria from a Workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `team/:team_Id/task`
- **Base URL:** `https://api.clickup.com/api/v2/`
- **Official documentation:** [List Filtered Team Tasks](https://developer.clickup.com/reference/getfilteredteamtasks)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `custom_items[]` | query | `array<number>` | no |
| `include_markdown_description` | query | `boolean` | no |
| `team_Id` | path | `list` | yes |
