# List Invoice Batches with Aspire

Retrieves invoice batches from your Aspire account.

## Endpoint

- **Method:** `GET`
- **Path:** `InvoiceBatches`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Invoice Batches](https://cloud-api.youraspire.com/swagger/index.html#/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
