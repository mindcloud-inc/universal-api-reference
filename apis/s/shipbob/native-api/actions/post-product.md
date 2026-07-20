# Post Product with ShipBob

## Endpoint

- **Method:** `POST`
- **Path:** `1.0/product`
- **Base URL:** `https://{apiSubdomain}.shipbob.com/`
- **API:** REST

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reference_id` | body | `string` | yes | — |
| `sku` | body | `string` | no | — |
| `name` | body | `string` | yes | — |
| `barcode` | body | `string` | no | — |
| `gtin` | body | `string` | no | Global Trade Item Number - unique and internationally recognized identifier assigned to item by company GS1. |
| `upc` | body | `string` | no | Universal Product Code - Unique external identifier |
| `unit_price` | body | `number` | no | The price of one unit |
