# List Products with Invoice Ninja

## Endpoint

- **Method:** `GET`
- **Path:** `/products`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [List Products](https://api-docs.invoicing.co/#tag/products/operation/getProducts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | no | Optional related records to include in the response. |
| `status` | query | `string` | no | Optional status filter such as active, archived, or deleted. |
