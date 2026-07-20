# List Service Types with Aspire

Retrieves service types from your Aspire account.

## Endpoint

- **Method:** `GET`
- **Path:** `ServiceTypes`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Service Types](https://cloud-api.youraspire.com/swagger/index.html#/ServiceTypes/ServiceTypes_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
