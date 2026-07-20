# Update Account with Outseta

Updates an existing account in Outseta.

## Endpoint

- **Method:** `PUT`
- **Path:** `/crm/accounts/:accountUid`
- **Base URL:** `https://{subdomain}.outseta.com/api/v1`
- **Official documentation:** [Update Account](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountUid` | path | `string` | yes |
| `Name` | body | `string` | no |
| `AccountStage` | body | `string` | no |
| `MailingAddress.Uid` | body | `string` | no |
| `MailingAddress.AddressLine1` | body | `string` | no |
| `MailingAddress.AddressLine2` | body | `string` | no |
| `BillingAddress.Uid` | body | `string` | no |
| `BillingAddress.AddressLine1` | body | `string` | no |
| `BillingAddress.AddressLine2` | body | `string` | no |
