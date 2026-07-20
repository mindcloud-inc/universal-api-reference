# Update Product with Paystack

## Endpoint

- **Method:** `PUT`
- **Path:** `/product/:productIdOrCode`
- **Base URL:** `https://api.paystack.co`
- **Official documentation:** [Update Product](https://paystack.com/docs/api/product/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productIdOrCode` | path | `string` | yes | Enter the numeric Paystack product id. The provider rejects product_code for this endpoint. |
| `name` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `price` | body | `number` | no | — |
| `currency` | body | `string` | no | — |
