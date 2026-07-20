# Delete Task with Wrike

Deletes an existing task from Wrike.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tasks/:taskId`
- **Base URL:** `https://{host}/api/v4`
- **Official documentation:** [Delete Task](https://developers.wrike.com/api/v4/tasks/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | Wrike task ID. |
