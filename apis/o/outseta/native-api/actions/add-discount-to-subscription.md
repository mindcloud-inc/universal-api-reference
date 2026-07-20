# Add Discount to Subscription with Outseta

Adds a discount to a subscription in Outseta.

## Endpoint

- **Method:** `POST`
- **Path:** `/billing/subscriptions/:subscriptionUid/discounts/:discountUid`
- **Base URL:** `https://{subdomain}.outseta.com/api/v1`
- **Official documentation:** [Add Discount to Subscription](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `subscriptionUid` | path | `string` | yes |
| `discountUid` | path | `string` | yes |
