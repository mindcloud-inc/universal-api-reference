# Create Task with Outlign

Creates a new task in Outlign.

## Endpoint

- **Method:** `POST`
- **Path:** `/steps`
- **Base URL:** `https://go.outlign.co/api/v1`
- **Official documentation:** [Create Task](https://go.outlign.co/api/docs/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Task title |
| `phase_id` | body | `number` | yes | Phase to attach the task to |
| `due_date` | body | `string` | no | Task due date |
