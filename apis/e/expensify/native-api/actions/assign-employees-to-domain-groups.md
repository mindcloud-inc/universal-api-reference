# Assign Employees To Domain Groups with Expensify

Updates employee domain group assignments in Expensify.

## Endpoint

- **Method:** `POST`
- **Path:** `ExpensifyIntegrations`
- **Base URL:** `https://integrations.expensify.com/Integration-Server/`
- **Official documentation:** [Assign Employees To Domain Groups](https://integrations.expensify.com/Integration-Server/doc/employeeUpdater/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeesJson` | body | `string` | yes | JSON array of employee objects for the Advanced Employee Updater request-mode feed. |
