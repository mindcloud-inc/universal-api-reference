# Get Task with MILKEE

Retrieves a task from MILKEE.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:companyId/tasks/:taskId`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Get Task](https://apidocs.milkee.ch/api/resources/tasks.html#retrieve-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
| `task_id` | path | `string` | yes | The numeric MILKEE task ID used in the request path. |
