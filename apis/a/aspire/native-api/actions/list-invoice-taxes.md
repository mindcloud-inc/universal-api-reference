# List Invoice Taxes with Aspire

Retrieves invoice taxes from your Aspire account.

## Endpoint

- **Method:** `GET`
- **Path:** `InvoiceTaxes`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Invoice Taxes](https://cloud-api.youraspire.com/swagger/index.html#/InvoiceTaxes/InvoiceTaxes_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
