# List All Refund By Customer Id with Pabbly Subscription Billing

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/refund/:customerId`
- **Base URL:** `https://payments.pabbly.com/api`
- **Official documentation:** [List All Refund By Customer Id](https://apidocs.pabbly.com/#f6e74481-c273-4337-ac16-17ed5b233d61)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customer_id` | path | `string` | no |
| `invoice_id` | query | `string` | no |
| `plan_id` | query | `string` | no |
| `product_id` | query | `string` | no |
| `status` | query | `string` | no |
| `subscription_id` | query | `string` | no |
