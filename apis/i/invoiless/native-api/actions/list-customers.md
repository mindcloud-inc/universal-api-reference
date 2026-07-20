# List Customers with Invoiless

Retrieves customers from Invoiless.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers`
- **Base URL:** `https://api.invoiless.com/v1`
- **Official documentation:** [List Customers](https://docs.invoiless.com/guide/customers.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search by customer name, email, or phone. |
