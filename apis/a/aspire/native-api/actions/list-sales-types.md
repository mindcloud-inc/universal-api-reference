# List Sales Types with Aspire

Retrieves sales types from your Aspire account.

## Endpoint

- **Method:** `GET`
- **Path:** `SalesTypes`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Sales Types](https://guide.youraspire.com/apidocs)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
