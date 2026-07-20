# Dry Run Employee Sync From URL with Expensify

Retrieves a dry-run employee sync from a URL in Expensify.

## Endpoint

- **Method:** `POST`
- **Path:** `ExpensifyIntegrations`
- **Base URL:** `https://integrations.expensify.com/Integration-Server/`
- **Official documentation:** [Dry Run Employee Sync From URL](https://integrations.expensify.com/Integration-Server/doc/employeeUpdater/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feedUrl` | body | `string` | yes | HTTPS URL that Expensify should download the employee JSON feed from. |
| `feedUser` | body | `string` | no | Optional Basic Auth username for the employee feed URL. |
| `feedPassword` | body | `string` | no | Optional Basic Auth password for the employee feed URL. |
