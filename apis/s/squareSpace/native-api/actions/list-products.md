# List Products with SquareSpace

Retrieves products from Squarespace.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/commerce/products`
- **Base URL:** `https://api.squarespace.com`
- **Official documentation:** [List Products](https://developers.squarespace.com/commerce-apis/products#list-products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifiedAfter` | query | `date` | no | Return products modified after this datetime. |
| `modifiedBefore` | query | `date` | no | Return products modified before this datetime. |
| `type` | query | `list<string>` | no | Filter products by type. Accepted values: `DIGITAL`, `GIFT_CARD`, `PHYSICAL`, `SERVICE`. |
