# Create Task with Time Doctor

Creates a new task in Time Doctor.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/tasks`
- **Base URL:** `https://api2.timedoctor.com`
- **Official documentation:** [Create Task](https://api2.timedoctor.com/#operation/createTask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Task name. |
| `description` | body | `string` | no | Task description. |
