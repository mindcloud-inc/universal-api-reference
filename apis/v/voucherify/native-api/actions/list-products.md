# List Products with Voucherify

Retrieves a list of products from Voucherify.

## Endpoint

- **Method:** `GET`
- **Path:** `/products`
- **Base URL:** `https://us1.api.voucherify.io/v1`
- **Official documentation:** [List Products](https://docs.voucherify.io/reference/list-products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number for paginated product results. |
| `limit` | query | `number` | no | Maximum number of products to return. |
