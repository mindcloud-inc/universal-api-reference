# List Equipment Service Logs with Aspire

Retrieves equipment service logs from your Aspire account.

## Endpoint

- **Method:** `GET`
- **Path:** `EquipmentServiceLogs`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Equipment Service Logs](https://cloud-api.youraspire.com/swagger/index.html#/EquipmentServiceLogs/EquipmentServiceLogs_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
