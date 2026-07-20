# Submit Workflow Task with Jodoo

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.jodoo.com/api/v1/workflow/task/approve`
- **Base URL:** `https://api.jodoo.com/api/v5`
- **Official documentation:** [Submit Workflow Task](https://help.jodoo.com/en/articles/9992447-workflow-tasks-submit-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | body | `string` | yes | Username assigned to the workflow task. |
| `instance_id` | body | `string` | yes | Workflow instance ID, which is the same as the record data ID. |
| `task_id` | body | `string` | yes | Workflow task ID assigned to the username. |
| `comment` | body | `string` | no | Optional approval comment. |
