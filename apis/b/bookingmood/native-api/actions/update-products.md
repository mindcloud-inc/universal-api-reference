# Update Products with Bookingmood

Updates product records in the Bookingmood API.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/products`
- **Base URL:** `https://api.bookingmood.com/v1`
- **Official documentation:** [Update Products](https://www.bookingmood.com/en-US/api-reference/products)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Filter the product by id using PostgREST syntax. |
| `name.default` | body | `string` | yes | Localized product name. |
