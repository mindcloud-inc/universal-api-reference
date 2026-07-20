# Retrieve Task with BrowserAct

Retrieves a task from BrowserAct.

## Endpoint

- **Method:** `GET`
- **Path:** `/get-task`
- **Base URL:** `https://api.browseract.com/v2/workflow`
- **Official documentation:** [Retrieve Task](https://docs.browseract.com/api-reference/tasks/retrieve-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | query | `string` | yes | Task ID returned by a BrowserAct task run. |
