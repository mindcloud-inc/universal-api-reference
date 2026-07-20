# List Tasks with Planfix

Retrieves tasks from Planfix.

## Endpoint

- **Method:** `POST`
- **Path:** `/task/list`
- **Base URL:** `{accountBaseUrl}/rest`
- **Official documentation:** [List Tasks](https://help.planfix.com/restapidocs/#/Task/get-task-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | body | `string` | no | Comma-separated task fields to return, for example id,name,description. |
| `pageSize` | body | `number` | no | Number of tasks to return per request. Planfix allows 1 to 100. |
| `offset` | body | `number` | no | Zero-based offset from the beginning of the task list. |
| `filterId` | body | `string` | no | Optional Planfix task filter ID, for example out. |
| `runAsUserId` | body | `string` | no | Run the request on behalf of a specific employee or contact, for example user:2. Admin-only. |
