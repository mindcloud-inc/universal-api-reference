# Update Project with FreshBooks

Updates an existing project in FreshBooks for a business.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/business/:businessId/project/:projectId`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [Update Project](https://www.freshbooks.com/api/project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | path | `string` | yes | FreshBooks business ID. |
| `projectId` | path | `string` | yes | FreshBooks project ID. |
| `project.title` | body | `string` | no | Project title. |
| `project.client_id` | body | `number` | no | FreshBooks client ID. |
| `project.project_type` | body | `string` | no | FreshBooks project type. |
| `project.fixed_price` | body | `string` | no | Fixed-price amount. |
| `project.rate` | body | `string` | no | Hourly rate amount. |
| `project.description` | body | `string` | no | Project description. |
