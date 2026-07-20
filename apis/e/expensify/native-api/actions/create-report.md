# Create Report with Expensify

Creates a new report in Expensify.

## Endpoint

- **Method:** `POST`
- **Path:** `ExpensifyIntegrations`
- **Base URL:** `https://integrations.expensify.com/Integration-Server/`
- **Official documentation:** [Create Report](https://integrations.expensify.com/Integration-Server/doc/#report-creator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policyId` | body | `string` | yes | The policy to create the report in. |
| `employeeEmail` | body | `string` | yes | The account that should own the created report. |
| `reportTitle` | body | `string` | yes | The title of the report to create. |
| `expensesJson` | body | `string` | yes | JSON array of expense objects to create on the report. |
