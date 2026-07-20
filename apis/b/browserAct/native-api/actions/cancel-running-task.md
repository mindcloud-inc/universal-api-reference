# Cancel Running Task with BrowserAct

Updates a running task in BrowserAct to cancel execution.

## Endpoint

- **Method:** `PUT`
- **Path:** `/stop-task`
- **Base URL:** `https://api.browseract.com/v2/workflow`
- **Official documentation:** [Cancel Running Task](https://docs.browseract.com/api-reference/tasks/cancel-a-running-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | query | `string` | yes | The BrowserAct task ID to cancel. |
| `biz_code` | query | `number` | no | Optional business cancellation code for your own tracking. |
