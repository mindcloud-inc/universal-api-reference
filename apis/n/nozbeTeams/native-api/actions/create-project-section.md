# Create Project Section with Nozbe Teams

Creates a new project section in Nozbe Teams.

## Endpoint

- **Method:** `POST`
- **Path:** `/project_sections`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Create Project Section](https://api4.nozbe.com/v1/api#/project_sections/postProjectSection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | The project that owns the section. |
| `name` | body | `string` | yes | The section name. |
| `position` | body | `number` | no | Optional sidebar position for the section. |
