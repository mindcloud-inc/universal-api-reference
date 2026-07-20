# Create Project Section with Nozbe Personal

Creates a new project section in Nozbe Personal.

## Endpoint

- **Method:** `POST`
- **Path:** `/project_sections`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Create Project Section](https://api4.nozbe.com/v1/api#/project_sections/postProjectSection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | Project that owns the section. |
| `name` | body | `string` | yes | Section name. |
| `position` | body | `number` | no | Section ordering position. |
