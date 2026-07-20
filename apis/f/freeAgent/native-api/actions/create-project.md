# Create Project with FreeAgent

Creates a new project in FreeAgent.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://api.freeagent.com/v2`
- **Official documentation:** [Create Project](https://dev.freeagent.com/docs/projects#create-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | body | `object` | no | Project payload. |
| `project.contact` | body | `string` | yes | Contact to bill for the project. |
| `project.name` | body | `string` | yes | Free-text project name. |
| `project.status` | body | `string` | yes | Project status. |
| `project.currency` | body | `string` | yes | Project currency code. |
| `project.budget_units` | body | `string` | yes | Budget units. |
| `project.budget` | body | `number` | no | Project budget. |
| `project.normal_billing_rate` | body | `number` | no | Normal billing rate. |
| `project.billing_period` | body | `string` | no | Billing period. |
