# Get Return Details with Loop Returns

Get the details of a specific return based on a return’s ID, an order name, or a Shopify order ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/warehouse/return/details`
- **Base URL:** `https://api.loopreturns.com/api/v1`
- **Official documentation:** [Get Return Details](https://docs.loopreturns.com/api-reference/latest/return-data/get-return-details)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `return_id` | query | `string` | no |
| `order_id` | query | `string` | no |
| `order_name` | query | `string` | no |
| `currency_type` | query | `string` | no |
