# Move Task with Dart

Moves a task within a Dart dartboard.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:id/move`
- **Base URL:** `https://app.dartai.com/api/v0/public`
- **Official documentation:** [Move Task](https://app.dartai.com/api/v0/public/docs/#/Task/moveTask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `afterTaskId` | body | `string` | no |
| `beforeTaskId` | body | `string` | no |
| `id` | path | `string` | no |
