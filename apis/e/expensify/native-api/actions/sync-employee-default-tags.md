# Sync Employee Default Tags with Expensify

Updates employee default tags in Expensify.

## Endpoint

- **Method:** `POST`
- **Path:** `ExpensifyIntegrations`
- **Base URL:** `https://integrations.expensify.com/Integration-Server/`
- **Official documentation:** [Sync Employee Default Tags](https://integrations.expensify.com/Integration-Server/doc/employeeUpdater/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeesJson` | body | `string` | yes | JSON array of employee objects for the Advanced Employee Updater request-mode feed. |
