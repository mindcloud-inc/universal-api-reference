# List Products with Stripe

## Endpoint

- **Method:** `GET`
- **Path:** `products`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [List Products](https://docs.stripe.com/api/products/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | query | `boolean` | no | Only return products that are active or inactive. |
| `created` | query | `object` | no | Only return products created during a date interval. |
| `created[gt]` | query | `date` | no | Minimum creation timestamp, exclusive. |
| `created[gte]` | query | `date` | no | Minimum creation timestamp, inclusive. |
| `created[lt]` | query | `date` | no | Maximum creation timestamp, exclusive. |
| `created[lte]` | query | `date` | no | Maximum creation timestamp, inclusive. |
| `ids[]` | query | `array<string>` | no | Only return products with the given IDs. Send multiple values as a array. |
| `shippable` | query | `boolean` | no | Only return products that can be shipped. |
| `url` | query | `string` | no | Only return products with the given URL. |
