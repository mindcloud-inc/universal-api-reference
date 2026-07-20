# Add First Time Subscription Preview with Outseta

Retrieves a first-time subscription charge preview from Outseta.

## Endpoint

- **Method:** `POST`
- **Path:** `/billing/subscriptions/compute-charge-summary`
- **Base URL:** `https://{subdomain}.outseta.com/api/v1`
- **Official documentation:** [Add First Time Subscription Preview](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `asOf` | query | `string` | no |
| `Plan.Uid` | body | `string` | no |
| `BillingRenewalTerm` | body | `number` | no |
| `Account` | body | `object` | no |
