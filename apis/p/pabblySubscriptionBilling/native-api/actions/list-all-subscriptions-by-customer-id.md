# List All Subscriptions By Customer Id with Pabbly Subscription Billing

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/subscriptions/:customerId`
- **Base URL:** `https://payments.pabbly.com/api`
- **Official documentation:** [List All Subscriptions By Customer Id](https://apidocs.pabbly.com/#cfd67f09-fea5-45ea-939e-7d10987806a1)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billing_cycle` | query | `string` | no | Supported value: onetime,lifetime,specific |
| `billing_period` | query | `string` | no | Supported value: w,m,y |
| `customer_id` | path | `string` | no | Pabbly Customer ID. |
| `plan_id` | query | `string` | no | Uniquely identifies the plan. |
| `product_id` | query | `string` | no | Uniquely identifies the product. |
| `status` | query | `string` | no | Supported subscription status such as live, pending, cancelled, expired, dunning, trial, nonrenewing, unpaid, or paused. |
