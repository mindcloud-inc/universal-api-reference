# Create Contact with Avaza

Creates a new contact in Avaza.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Contact`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Create Contact](https://api.avaza.com/#!/Contact/Contact_Post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `CompanyIDFK` | body | `number` | no |
| `CompanyName` | body | `string` | no |
| `CurrencyCode` | body | `string` | no |
| `CompanyBillingAddress` | body | `string` | no |
| `CompanyBillingAddressLine` | body | `string` | no |
| `CompanyBillingAddressCity` | body | `string` | no |
| `CompanyBillingAddressState` | body | `string` | no |
| `CompanyBillingAddressPostCode` | body | `string` | no |
| `CompanyBillingAddressCountryCode` | body | `string` | no |
| `ContactEmail` | body | `string` | yes |
| `Firstname` | body | `string` | yes |
| `Lastname` | body | `string` | yes |
| `PositionTitle` | body | `string` | no |
| `Mobile` | body | `string` | no |
| `Phone` | body | `string` | no |
| `UpdateExisting` | body | `boolean` | no |
