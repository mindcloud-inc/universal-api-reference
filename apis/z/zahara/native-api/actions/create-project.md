# Create Project with Zahara

Creates a new project in Zahara.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/{businessUnitApiKey}/Project/Add`
- **Base URL:** `https://api.myzahara.net`
- **Official documentation:** [Create Project](https://ask.zaharasoftware.com/api-docs/add-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProjectName` | body | `string` | yes | Project name. |
| `ProjectCode` | body | `string` | yes | Project code. |
| `Description` | body | `string` | yes | Project description. |
| `BudgetedAmount` | body | `number` | yes | Budgeted amount. |
| `Start` | body | `date` | yes | Project start date. |
| `End` | body | `date` | yes | Project end date. |
