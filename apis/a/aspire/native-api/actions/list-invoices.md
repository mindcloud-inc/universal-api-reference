# List Invoices with Aspire

## Endpoint

- **Method:** `GET`
- **Path:** `invoices`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Invoices](https://guide.youraspire.com/apidocs/invoices-4)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
