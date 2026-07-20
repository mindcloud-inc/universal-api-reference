# Add Account with Subscription with Outseta

Creates an account with a subscription in Outseta.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/accounts`
- **Base URL:** `https://{subdomain}.outseta.com/api/v1`
- **Official documentation:** [Add Account with Subscription](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Name` | body | `string` | no |
| `MailingAddress.AddressLine1` | body | `string` | no |
| `MailingAddress.AddressLine2` | body | `string` | no |
| `MailingAddress.City` | body | `string` | no |
| `MailingAddress.State` | body | `string` | no |
| `MailingAddress.PostalCode` | body | `string` | no |
| `BillingAddress.AddressLine1` | body | `string` | no |
| `BillingAddress.AddressLine2` | body | `string` | no |
| `BillingAddress.City` | body | `string` | no |
| `BillingAddress.State` | body | `string` | no |
| `BillingAddress.PostalCode` | body | `string` | no |
| `PersonAccount[].Person.Uid` | body | `string` | no |
| `PersonAccount[].IsPrimary` | body | `string` | no |
| `Subscriptions[].Plan.Uid` | body | `string` | no |
| `Subscriptions[].BillingRenewalTerm` | body | `number` | no |
