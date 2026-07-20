# List Contact Custom Fields with Aspire

Retrieves contact custom fields from your Aspire account.

## Endpoint

- **Method:** `GET`
- **Path:** `ContactCustomFields`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Contact Custom Fields](https://guide.youraspire.com/apidocs/propertycustomfields-7)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
