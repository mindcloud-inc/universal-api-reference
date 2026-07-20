# Create Project with FreshBooks

Creates a new project in FreshBooks for a business.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/business/:businessId/project`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [Create Project](https://www.freshbooks.com/api/project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | path | `string` | yes | FreshBooks business ID. |
| `project.title` | body | `string` | yes | Project title. |
| `project.client_id` | body | `number` | yes | FreshBooks client ID. |
| `project.project_type` | body | `string` | yes | FreshBooks project type. |
| `project.fixed_price` | body | `string` | no | Fixed-price amount. |
| `project.rate` | body | `string` | no | Hourly rate amount. |
| `project.description` | body | `string` | no | Project description. |
