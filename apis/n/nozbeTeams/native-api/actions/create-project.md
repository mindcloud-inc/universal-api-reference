# Create Project with Nozbe Teams

Creates a new project in Nozbe Teams.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Create Project](https://api4.nozbe.com/v1/api#/projects/postProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The project name. |
| `team_id` | body | `string` | yes | The team that will own the project. |
| `is_open` | body | `boolean` | yes | Whether the project is open. |
| `is_template` | body | `boolean` | no | Whether the project should be created as a template. |
