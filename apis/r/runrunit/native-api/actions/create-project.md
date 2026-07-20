# Create Project with Runrun.it

Creates a new project in Runrun.it.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [Create Project](https://runrun.it/api/documentation#projects-create-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project.name` | body | `string` | yes | Project name. |
| `project.client_id` | body | `number` | yes | Client ID for the project. |
| `project.start_date` | body | `date` | no | Project start date. |
| `project.desired_date` | body | `date` | no | Desired delivery date for the project. |
