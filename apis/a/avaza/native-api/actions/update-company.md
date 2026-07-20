# Update Company with Avaza

Updates an existing company in Avaza.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/Company`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Update Company](https://api.avaza.com/#!/Company/Company_Put)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `CompanyID` | body | `number` | no |
| `FieldsToUpdate` | body | `list<string>` | yes |
| `CompanyName` | body | `string` | no |
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
