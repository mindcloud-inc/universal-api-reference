# List Tasks with BrowserAct

Retrieves tasks from BrowserAct.

## Endpoint

- **Method:** `GET`
- **Path:** `/list-tasks`
- **Base URL:** `https://api.browseract.com/v2/workflow`
- **Official documentation:** [List Tasks](https://docs.browseract.com/api-reference/tasks/list-tasks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Optional BrowserAct task status filter. |
| `workflow_id` | query | `string` | no | Optional workflow ID filter. |
