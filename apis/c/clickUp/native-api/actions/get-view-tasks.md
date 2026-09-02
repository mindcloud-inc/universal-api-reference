# Get View Tasks with ClickUp

Retrieves visible tasks from a ClickUp view.

## Endpoint

- **Method:** `GET`
- **Path:** `view/:view_id/task`
- **Base URL:** `https://api.clickup.com/api/v2/`
- **Official documentation:** [Get View Tasks](https://developer.clickup.com/reference/createlist)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `view_id` | path | `string` | yes |
