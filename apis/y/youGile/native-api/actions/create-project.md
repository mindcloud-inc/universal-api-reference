# Create project with YouGile

Creates a new project in YouGile.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `{companyDomain}/api-v2`
- **Official documentation:** [Create project](https://ru.yougile.com/api-v2#/operations/ProjectController_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The project title. |
| `users` | body | `object` | no | Map of user IDs to project roles. |
