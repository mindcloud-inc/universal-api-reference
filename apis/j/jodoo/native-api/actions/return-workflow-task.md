# Return Workflow Task with Jodoo

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.jodoo.com/api/v1/workflow/task/rollback`
- **Base URL:** `https://api.jodoo.com/api/v5`
- **Official documentation:** [Return Workflow Task](https://help.jodoo.com/en/articles/9992426-workflow-tasks-return-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | body | `string` | yes | Username assigned to the workflow task. |
| `instance_id` | body | `string` | yes | Workflow instance ID, which is the same as the record data ID. |
| `task_id` | body | `string` | yes | Workflow task ID assigned to the username. |
| `flow_id` | body | `number` | no | Optional flow node ID to return to. |
| `comment` | body | `string` | no | Optional approval comment. |
