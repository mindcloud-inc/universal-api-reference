# Retrieve Task Status with BrowserAct

Retrieves the current status of a task from BrowserAct.

## Endpoint

- **Method:** `GET`
- **Path:** `/get-task-status`
- **Base URL:** `https://api.browseract.com/v2/workflow`
- **Official documentation:** [Retrieve Task Status](https://docs.browseract.com/api-reference/tasks/retrieve-a-task-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | query | `string` | yes | Task ID returned by a BrowserAct task run. |
