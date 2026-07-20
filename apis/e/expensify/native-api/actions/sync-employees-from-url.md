# Sync Employees From URL with Expensify

Updates employees in Expensify from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `ExpensifyIntegrations`
- **Base URL:** `https://integrations.expensify.com/Integration-Server/`
- **Official documentation:** [Sync Employees From URL](https://integrations.expensify.com/Integration-Server/doc/employeeUpdater/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feedUrl` | body | `string` | yes | HTTPS URL that Expensify should download the employee JSON feed from. |
| `feedUser` | body | `string` | no | Optional Basic Auth username for the employee feed URL. |
| `feedPassword` | body | `string` | no | Optional Basic Auth password for the employee feed URL. |
