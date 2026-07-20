# Add Add-On to Subscription with Outseta

Adds an add-on to a subscription in Outseta.

## Endpoint

- **Method:** `POST`
- **Path:** `/billing/subscriptionaddons`
- **Base URL:** `https://{subdomain}.outseta.com/api/v1`
- **Official documentation:** [Add Add-On to Subscription](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `AddOn.Uid` | body | `string` | no |
| `BillingRenewalTerm` | body | `number` | no |
| `Quantity` | body | `number` | no |
| `Subscription.Uid` | body | `string` | no |
