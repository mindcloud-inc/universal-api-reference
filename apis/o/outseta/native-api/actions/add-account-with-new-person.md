# Add Account with New Person with Outseta

Creates an account with a new person in Outseta.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/accounts`
- **Base URL:** `https://{subdomain}.outseta.com/api/v1`
- **Official documentation:** [Add Account with New Person](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sendConfirmationEmail` | query | `boolean` | no |
| `Name` | body | `string` | no |
| `AccountStage` | body | `string` | no |
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
| `PersonAccount[].Person.Email` | body | `string` | no |
| `PersonAccount[].Person.FirstName` | body | `string` | no |
| `PersonAccount[].Person.LastName` | body | `string` | no |
| `PersonAccount[].IsPrimary` | body | `string` | no |
