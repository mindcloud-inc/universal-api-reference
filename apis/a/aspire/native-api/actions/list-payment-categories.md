# List Payment Categories with Aspire

Retrieves payment categories from your Aspire account.

## Endpoint

- **Method:** `GET`
- **Path:** `PaymentCategories`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Payment Categories](https://cloud-api.youraspire.com/swagger/index.html#/PaymentCategories/PaymentCategories_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
