# Create Project with Nozbe Personal

Creates a new project in Nozbe Personal.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Create Project](https://api4.nozbe.com/v1/api#/projects/postProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Project name. |
| `team_id` | body | `string` | yes | Team ID for the project. |
| `is_open` | body | `boolean` | yes | Whether the project is open. |
| `is_template` | body | `boolean` | no | Whether the project should be created as a template. |
