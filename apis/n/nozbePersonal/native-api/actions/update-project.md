# Update Project with Nozbe Personal

Updates an existing project in Nozbe Personal.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:id`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Update Project](https://api4.nozbe.com/v1/api#/projects/putProjectById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Project ID to update. |
| `name` | body | `string` | no | Updated project name. |
| `is_template` | body | `boolean` | no | Whether the project is a template. |
