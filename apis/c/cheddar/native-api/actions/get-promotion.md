# Get Promotion with Cheddar

Retrieves promotion coupon details from Cheddar.

## Endpoint

- **Method:** `GET`
- **Path:** `/promotions/get/productCode/{productCode}/code/:promotionCode`
- **Base URL:** `https://getcheddar.com/xml`
- **Official documentation:** [Get Promotion](https://docs.getcheddar.com/#get-a-single-promotions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Promotion code from Cheddar. |
