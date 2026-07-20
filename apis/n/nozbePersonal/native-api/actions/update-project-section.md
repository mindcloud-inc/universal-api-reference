# Update Project Section with Nozbe Personal

Updates an existing project section in Nozbe Personal.

## Endpoint

- **Method:** `PUT`
- **Path:** `/project_sections/:id`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Update Project Section](https://api4.nozbe.com/v1/api#/project_sections/putProjectSectionById)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
| `position` | body | `number` | no |
