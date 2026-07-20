# Update a Task with Beebole

Updates an existing task in Beebole.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://beebole-apps.com/api/v2`
- **Official documentation:** [Update a Task](https://beebole.com/help/api#update-a-task)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task.id` | body | `number` | yes |
| `task.name` | body | `string` | no |
