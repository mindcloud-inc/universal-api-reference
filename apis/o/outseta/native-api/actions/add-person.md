# Add Person with Outseta

Creates a new person in Outseta.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/people`
- **Base URL:** `https://{subdomain}.outseta.com/api/v1`
- **Official documentation:** [Add Person](https://documenter.getpostman.com/view/3613332/outseta-rest-api-v1/7TNfr6k)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Email` | body | `string` | no |
| `FirstName` | body | `string` | no |
| `LastName` | body | `string` | no |
| `MailingAddress.AddressLine1` | body | `string` | no |
| `MailingAddress.AddressLine2` | body | `string` | no |
| `MailingAddress.AddressLine3` | body | `string` | no |
| `MailingAddress.City` | body | `string` | no |
| `MailingAddress.State` | body | `string` | no |
| `MailingAddress.PostalCode` | body | `string` | no |
