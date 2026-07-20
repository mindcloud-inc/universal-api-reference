# Update project with YouGile

Updates an existing project in YouGile.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:id`
- **Base URL:** `{companyDomain}/api-v2`
- **Official documentation:** [Update project](https://ru.yougile.com/api-v2#/operations/ProjectController_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The YouGile project ID. |
| `title` | body | `string` | no | The updated project title. |
| `users` | body | `object` | no | Updated map of user IDs to project roles. |
| `deleted` | body | `boolean` | no | Mark the project as deleted. |
