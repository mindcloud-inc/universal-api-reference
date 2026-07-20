# Transfer Workflow Task with Jodoo

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.jodoo.com/api/v1/workflow/task/transfer`
- **Base URL:** `https://api.jodoo.com/api/v5`
- **Official documentation:** [Transfer Workflow Task](https://help.jodoo.com/en/articles/9992428-workflow-tasks-transfer-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | body | `string` | yes | Username currently assigned to the workflow task. |
| `instance_id` | body | `string` | yes | Workflow instance ID, which is the same as the record data ID. |
| `task_id` | body | `string` | yes | Workflow task ID assigned to the username. |
| `transfer_username` | body | `string` | yes | Username that should receive the task. |
| `comment` | body | `string` | no | Optional transfer comment. |
