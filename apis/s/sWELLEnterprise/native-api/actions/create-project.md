# Create Project with SWELLEnterprise

Creates a new project in SWELLEnterprise.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/projects`
- **Base URL:** `https://dashboard.swellsystem.com/api/v1`
- **Official documentation:** [Create Project](https://dashboard.swellsystem.com/docs#projects-POSTapi-v1-projects-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The project name. |
| `status` | body | `string` | no | The project status. |
| `company_id` | body | `number` | no | The company ID. |
| `contact_id` | body | `number` | no | The contact ID. |
