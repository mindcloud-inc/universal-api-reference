# Update Project Section with Nozbe Teams

Updates an existing project section in Nozbe Teams.

## Endpoint

- **Method:** `PUT`
- **Path:** `/project_sections/:id`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Update Project Section](https://api4.nozbe.com/v1/api#/project_sections/putProjectSectionById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The project section to update. |
| `name` | body | `string` | no | The updated section name. |
| `position` | body | `number` | no | Optional sidebar position for the section. |
