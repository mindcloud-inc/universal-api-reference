# Update Task with Outlign

Updates an existing task in Outlign.

## Endpoint

- **Method:** `PUT`
- **Path:** `/steps/:id`
- **Base URL:** `https://go.outlign.co/api/v1`
- **Official documentation:** [Update Task](https://go.outlign.co/api/docs/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Task ID |
| `title` | body | `string` | no | Updated task title |
