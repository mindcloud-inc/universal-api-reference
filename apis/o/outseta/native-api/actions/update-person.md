# Update Person with Outseta

Updates an existing person in Outseta.

## Endpoint

- **Method:** `PUT`
- **Path:** `/crm/people/:personUid`
- **Base URL:** `https://{subdomain}.outseta.com/api/v1`
- **Official documentation:** [Update Person](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `personUid` | path | `string` | yes |
| `Email` | body | `string` | no |
| `FirstName` | body | `string` | no |
| `LastName` | body | `string` | no |
| `MailingAddress.Uid` | body | `string` | no |
| `MailingAddress.AddressLine1` | body | `string` | no |
| `MailingAddress.AddressLine2` | body | `string` | no |
| `MailingAddress.AddressLine3` | body | `string` | no |
| `MailingAddress.City` | body | `string` | no |
| `MailingAddress.State` | body | `string` | no |
| `MailingAddress.PostalCode` | body | `string` | no |
