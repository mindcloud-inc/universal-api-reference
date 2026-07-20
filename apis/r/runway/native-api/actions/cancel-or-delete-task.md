# Cancel Or Delete Task with Runway

Cancels or deletes a task in Runway.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/tasks/[:id]`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Cancel Or Delete Task](https://docs.dev.runwayml.com/api#tag/Task-management/paths/~1v1~1tasks~1%7Bid%7D/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | UUID of a previously submitted task. |
