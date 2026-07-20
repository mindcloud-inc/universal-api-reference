# Create Task with Kiwili

Creates a new task in Kiwili.

## Endpoint

- **Method:** `POST`
- **Path:** `/task`
- **Base URL:** `https://mindcloud.kiwili.com/api`
- **Official documentation:** [Create Task](https://api.kiwili.com/api/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Active` | body | `boolean` | no | Whether the task is active. |
| `EnterpriseId` | body | `number` | yes | The enterprise ID for the task. |
| `ProjectId` | body | `number` | yes | The project ID for the task. |
| `Summary` | body | `string` | yes | The task summary. |
