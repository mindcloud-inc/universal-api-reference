# Delete Task with Time Doctor

Archives or restores a task in Time Doctor.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/1.0/tasks/:taskId`
- **Base URL:** `https://api2.timedoctor.com`
- **Official documentation:** [Delete Task](https://api2.timedoctor.com/#operation/deleteTask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | ID of the task to delete. |
