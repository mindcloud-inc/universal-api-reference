# Add First Time Subscription with Outseta

Adds a first-time subscription in Outseta.

## Endpoint

- **Method:** `PUT`
- **Path:** `/billing/subscriptions/firsttimesubscription`
- **Base URL:** `https://{subdomain}.outseta.com/api/v1`
- **Official documentation:** [Add First Time Subscription](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Plan.Uid` | body | `string` | no |
| `BillingRenewalTerm` | body | `number` | no |
| `Account.Uid` | body | `string` | no |
