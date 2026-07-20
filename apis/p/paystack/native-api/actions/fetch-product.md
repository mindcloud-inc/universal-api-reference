# Fetch Product with Paystack

## Endpoint

- **Method:** `GET`
- **Path:** `/product/:productIdOrCode`
- **Base URL:** `https://api.paystack.co`
- **Official documentation:** [Fetch Product](https://paystack.com/docs/api/product/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productIdOrCode` | path | `string` | yes | Enter the numeric Paystack product id. The provider rejects product_code for this endpoint. |
