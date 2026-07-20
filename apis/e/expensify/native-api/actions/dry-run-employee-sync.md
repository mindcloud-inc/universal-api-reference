# Dry Run Employee Sync with Expensify

Retrieves a dry-run employee sync result from Expensify.

## Endpoint

- **Method:** `POST`
- **Path:** `ExpensifyIntegrations`
- **Base URL:** `https://integrations.expensify.com/Integration-Server/`
- **Official documentation:** [Dry Run Employee Sync](https://integrations.expensify.com/Integration-Server/doc/employeeUpdater/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeesJson` | body | `string` | yes | JSON array of employee objects for the Advanced Employee Updater request-mode feed. |
