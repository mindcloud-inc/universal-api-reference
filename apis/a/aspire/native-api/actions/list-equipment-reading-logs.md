# List Equipment Reading Logs with Aspire

Retrieves equipment reading logs from your Aspire account.

## Endpoint

- **Method:** `GET`
- **Path:** `EquipmentReadingLogs`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Equipment Reading Logs](https://cloud-api.youraspire.com/swagger/index.html#/EquipmentReadingLogs/EquipmentReadingLogs_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
