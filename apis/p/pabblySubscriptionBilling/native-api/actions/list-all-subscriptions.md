# List All Subscriptions with Pabbly Subscription Billing

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/subscriptions`
- **Base URL:** `https://payments.pabbly.com/api`
- **Official documentation:** [List All Subscriptions](https://apidocs.pabbly.com/#30d9b403-4bc2-49de-bdf8-b4147a55fb5c)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billing_cycle` | query | `string` | no | Supported value: onetime,lifetime,specific |
| `billing_period` | query | `string` | no | Supported value: w,m,y |
| `plan_id` | query | `string` | no | Uniquely identifies the plan. |
| `product_id` | query | `string` | no | Uniquely identifies the product. |
| `status` | query | `string` | no | Supported subscription status such as live, pending, cancelled, expired, dunning, trial, nonrenewing, unpaid, or paused. |
