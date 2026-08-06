# Post Product with ShipBob

## Endpoint

- **Method:** `POST`
- **Path:** `2026-07/product`
- **Base URL:** `https://{apiSubdomain}.shipbob.com/`
- **API:** REST
- **Official documentation:** [Post Product](https://developer-stage.shipbob.dev/2026-07/api/products/create-product)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `is_quarantine` | body | `string` | no | — |
| `variants[].sku` | body | `string` | no | — |
| `name` | body | `string` | no | — |
| `variants[].upc` | body | `string` | no | — |
| `taxonomy_id` | body | `number` | no | — |
| `type_id` | body | `number` | no | The product type ID (1 = Regular, 2 = Bundle) |
| `variants[]` | body | `array<object>` | no | — |
