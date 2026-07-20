# Update Project with Zahara

Updates an existing project in Zahara.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/{businessUnitApiKey}/Project/Update/{{projectId}}`
- **Base URL:** `https://api.myzahara.net`
- **Official documentation:** [Update Project](https://ask.zaharasoftware.com/api-docs/update-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | The Zahara project ID to update. |
| `ProjectName` | body | `string` | yes | Project name. |
| `ProjectCode` | body | `string` | yes | Project code. |
| `Description` | body | `string` | yes | Project description. |
| `BudgetedAmount` | body | `number` | yes | Budgeted amount. |
| `Start` | body | `date` | yes | Project start date. |
| `End` | body | `date` | yes | Project end date. |
