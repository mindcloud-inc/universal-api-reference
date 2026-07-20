# Update Project with FreeAgent

Updates an existing project in FreeAgent.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:id`
- **Base URL:** `https://api.freeagent.com/v2`
- **Official documentation:** [Update Project](https://dev.freeagent.com/docs/projects#update-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | FreeAgent project ID. |
| `project` | body | `object` | no | Project payload. |
| `project.contact` | body | `string` | no | Contact to bill for the project. |
| `project.name` | body | `string` | no | Free-text project name. |
| `project.status` | body | `string` | no | Project status. |
| `project.currency` | body | `string` | no | Project currency code. |
| `project.budget_units` | body | `string` | no | Budget units. |
| `project.budget` | body | `number` | no | Project budget. |
| `project.normal_billing_rate` | body | `number` | no | Normal billing rate. |
| `project.billing_period` | body | `string` | no | Billing period. |
