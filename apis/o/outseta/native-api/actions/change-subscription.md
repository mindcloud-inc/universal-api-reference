# Change Subscription with Outseta

Changes an existing subscription in Outseta.

## Endpoint

- **Method:** `PUT`
- **Path:** `/billing/subscriptions/:subscriptionUid/changesubscription`
- **Base URL:** `https://{subdomain}.outseta.com/api/v1`
- **Official documentation:** [Change Subscription](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `subscriptionUid` | path | `string` | yes |
| `Plan.Uid` | body | `string` | no |
| `BillingRenewalTerm` | body | `number` | no |
| `Account.Uid` | body | `string` | no |
