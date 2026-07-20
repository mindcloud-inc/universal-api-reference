# Update Project with MILKEE

Updates an existing project in MILKEE.

## Endpoint

- **Method:** `PUT`
- **Path:** `/companies/:companyId/projects/:projectId`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Update Project](https://apidocs.milkee.ch/api/resources/projects.html#project-aktualisieren)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | body | `boolean` | no | Archive the project when true. |
| `budget` | body | `number` | no | Project budget amount. |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
| `customer_id` | body | `number` | no | Associated customer ID. |
| `end_date` | body | `string` | no | Project end date in YYYY-MM-DD format. |
| `hourly_rate` | body | `number` | no | Project hourly rate. |
| `kanban_status` | body | `string` | no | Custom kanban workflow status. |
| `name` | body | `string` | no | Project name. |
| `project` | path | `string` | yes | The numeric MILKEE project ID used in the request path. |
| `project_type` | body | `string` | no | Project type: byHour, fixedBudget, or fixedPrice. |
| `start_date` | body | `string` | no | Project start date in YYYY-MM-DD format. |
