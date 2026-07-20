# Create Company with Avaza

Creates a new company in Avaza.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Company`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Create Company](https://api.avaza.com/#!/Company/Company_Post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `CompanyName` | body | `string` | yes |
| `CurrencyCode` | body | `string` | no |
| `BillingAddressLine` | body | `string` | no |
| `BillingAddressCity` | body | `string` | no |
| `BillingAddressState` | body | `string` | no |
| `BillingAddressPostCode` | body | `string` | no |
| `BillingCountryCode` | body | `string` | no |
| `BillingAddress` | body | `string` | no |
| `Phone` | body | `string` | no |
| `Fax` | body | `string` | no |
| `website` | body | `string` | no |
| `TaxNumber` | body | `string` | no |
| `Comments` | body | `string` | no |
