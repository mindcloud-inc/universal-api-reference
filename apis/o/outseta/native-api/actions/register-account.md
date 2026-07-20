# Register Account with Outseta

Registers an account in Outseta.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/registrations`
- **Base URL:** `https://{subdomain}.outseta.com/api/v1`
- **Official documentation:** [Register Account](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Name` | body | `string` | no |
| `PersonAccount[].IsPrimary` | body | `boolean` | no |
| `PersonAccount[].Person.Email` | body | `string` | no |
| `Subscriptions[].BillingRenewalTerm` | body | `number` | no |
| `Subscriptions[].Plan.Uid` | body | `string` | no |
