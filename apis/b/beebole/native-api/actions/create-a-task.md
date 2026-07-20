# Create a Task with Beebole

Creates a new task in Beebole.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://beebole-apps.com/api/v2`
- **Official documentation:** [Create a Task](https://beebole.com/help/api#create-a-task)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task.name` | body | `string` | yes |
| `task.company.id` | body | `number` | yes |
