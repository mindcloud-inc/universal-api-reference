# Resume Paused Task with BrowserAct

Updates a paused task in BrowserAct to resume execution.

## Endpoint

- **Method:** `PUT`
- **Path:** `/resume-task`
- **Base URL:** `https://api.browseract.com/v2/workflow`
- **Official documentation:** [Resume Paused Task](https://docs.browseract.com/api-reference/tasks/resume-a-paused-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | query | `string` | yes | The BrowserAct task ID to resume. |
