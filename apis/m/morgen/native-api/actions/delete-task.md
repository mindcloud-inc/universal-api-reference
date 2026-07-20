# Delete Task with Morgen

Deletes a task from Morgen.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/tasks/delete`
- **Base URL:** `https://api.morgen.so`
- **Official documentation:** [Delete Task](https://docs.morgen.so/tasks#delete-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Morgen task ID. |
