# Sync Employees From SFTP with Expensify

Updates employees in Expensify from SFTP.

## Endpoint

- **Method:** `POST`
- **Path:** `ExpensifyIntegrations`
- **Base URL:** `https://integrations.expensify.com/Integration-Server/`
- **Official documentation:** [Sync Employees From SFTP](https://integrations.expensify.com/Integration-Server/doc/employeeUpdater/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sftpHost` | body | `string` | yes | SFTP host that Expensify should connect to for the employee feed. |
| `sftpLogin` | body | `string` | yes | SFTP username for the employee feed. |
| `sftpPassword` | body | `string` | yes | SFTP password for the employee feed. |
| `sftpFilename` | body | `string` | yes | Absolute SFTP path to the employee JSON feed. |
| `sftpPort` | body | `string` | no | SFTP port for the employee feed server. |
