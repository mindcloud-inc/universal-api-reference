# Update Task with Time Doctor

Updates an existing task in Time Doctor.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/1.0/tasks/:taskId`
- **Base URL:** `https://api2.timedoctor.com`
- **Official documentation:** [Update Task](https://api2.timedoctor.com/#operation/putTask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | ID of the task to update. |
| `name` | body | `string` | no | Task name. |
| `description` | body | `string` | no | Task description. |
