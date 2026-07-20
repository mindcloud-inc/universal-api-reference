# Update Task with Kiwili

Updates an existing task in Kiwili.

## Endpoint

- **Method:** `PUT`
- **Path:** `/task/:task_id`
- **Base URL:** `https://mindcloud.kiwili.com/api`
- **Official documentation:** [Update Task](https://api.kiwili.com/api/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Active` | body | `boolean` | no | Whether the task is active. |
| `EnterpriseId` | body | `number` | no | The enterprise ID for the task. |
| `ProjectId` | body | `number` | no | The project ID for the task. |
| `Summary` | body | `string` | no | The updated task summary. |
| `task_id` | path | `number` | yes | The Kiwili task ID to update. |
