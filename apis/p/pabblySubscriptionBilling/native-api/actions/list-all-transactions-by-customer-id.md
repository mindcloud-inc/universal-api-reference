# List All Transactions By Customer Id with Pabbly Subscription Billing

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/transactions/:customerId`
- **Base URL:** `https://payments.pabbly.com/api`
- **Official documentation:** [List All Transactions By Customer Id](https://apidocs.pabbly.com/#ee9ef738-1a1c-4a3f-a036-8b22b9a3c48a)

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
| `type` | query | `string` | no |
