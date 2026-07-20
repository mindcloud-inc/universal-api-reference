# List Customers with Syncro

Retrieves a list of customers from Syncro.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers`
- **Base URL:** `https://mindcloud.syncromsp.com/api/v1`
- **Official documentation:** [List Customers](https://api-docs.syncromsp.com/#/Customer/)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | General customer search text. |
| `firstname` | query | `string` | no | — |
| `lastname` | query | `string` | no | — |
| `business_name` | query | `string` | no | — |
| `id` | query | `number` | no | — |
| `not_id` | query | `number` | no | Exclude a specific customer ID from the results. |
| `email` | query | `string` | no | — |
| `include_disabled` | query | `boolean` | no | Include disabled customers in the results. |
| `sort` | query | `string` | no | Customer field and direction, for example firstname ASC. |
| `page` | query | `number` | no | — |
