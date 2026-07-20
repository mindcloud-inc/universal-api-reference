# Create Project with MILKEE

Creates a new project in MILKEE.

## Endpoint

- **Method:** `POST`
- **Path:** `/companies/:companyId/projects`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Create Project](https://apidocs.milkee.ch/api/resources/projects.html#neues-project-erstellen)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `budget` | body | `number` | no | Project budget amount. |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
| `customer_id` | body | `number` | no | Existing customer ID. Mutually exclusive with New Customer Name. |
| `hourly_rate` | body | `number` | no | Project hourly rate. |
| `name` | body | `string` | yes | Project name. |
| `newCustomerName` | body | `string` | no | Create a new customer and assign the project to it. Mutually exclusive with Customer ID. |
| `project_type` | body | `string` | no | Project type: byHour, fixedBudget, or fixedPrice. |
