# List Workflow Tasks with Jodoo

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.jodoo.com/api/v4/workflow/task/list`
- **Base URL:** `https://api.jodoo.com/api/v5`
- **Official documentation:** [List Workflow Tasks](https://help.jodoo.com/en/articles/9992446-workflow-tasks-query-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | body | `string` | yes | Username whose pending workflow tasks should be listed. |
| `skip` | body | `number` | no | Number of workflow tasks to skip. |
| `limit` | body | `number` | no | Maximum number of workflow tasks to return. |
