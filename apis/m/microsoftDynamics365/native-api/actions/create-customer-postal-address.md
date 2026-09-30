# Create Customer Postal Address with Microsoft Dynamics 365

## Endpoint

- **Method:** `POST`
- **Path:** `CustomerPostalAddresses`
- **Base URL:** `{baseURL}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataAreaId` | body | `string` | no | — |
| `addressDescription` | body | `string` | no | — |
| `customerLegalEntityId` | body | `string` | no | — |
| `customerAccountNumber` | body | `string` | no | — |
| `addressStreet` | body | `string` | no | — |
| `addressCity` | body | `string` | no | — |
| `addressState` | body | `string` | no | — |
| `addressZipCode` | body | `string` | no | — |
| `addressCountryRegionId` | body | `string` | no | — |
| `addressCountryRegionISOCode` | body | `string` | no | — |
| `isPostalAddress` | body | `string` | no | Yes/No |
| `isPrimary` | body | `string` | no | Yes/No |
| `isRoleBusiness` | body | `string` | no | Yes/No |
| `isPrivate` | body | `string` | no | Yes/No |
| `isPrivatePostalAddress` | body | `string` | no | Yes/No |
| `isPrimaryTaxRegistration` | body | `string` | no | Yes/No |
| `isRoleDelivery` | body | `string` | no | Yes/No |
| `addressLocationRoles` | body | `string` | no | — |
| `addressDefaultRoles` | body | `string` | no | — |
| `isRoleHome` | body | `string` | no | — |
| `isRoleInvoice` | body | `string` | no | — |
