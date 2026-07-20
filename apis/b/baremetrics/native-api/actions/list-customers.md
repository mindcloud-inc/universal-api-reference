# List Customers with Baremetrics

Retrieves customers from Baremetrics.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:source_id/customers`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [List Customers](https://developers.baremetrics.com/reference/list-customers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Allows you to search for a customer based on: oid, email, notes and name |
| `source_id` | path | `string` | yes | Please see [Sources](ref:sources) |
| `sort` | query | `string` | no | Allows you to sort the results. You can use ltv or created |
| `order` | query | `string` | no | — |
