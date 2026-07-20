# Update Ship-to Addresses SSI with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `PATCH`
- **Path:** `v2.0/companies(:company_id)/shipToAddressesSSI(CustomerNo=':customerNo',Code=':shipToAddressCode')`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/ssi/aapi/`
- **API:** REST (Copy)
- **Official documentation:** [Update Ship-to Addresses SSI](https://anotepad.com/notes/x8dnaab8)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_id` | path | `string` | no |
| `code` | body | `string` | no |
| `customerNo` | path | `string` | no |
| `shipToAddressCode` | path | `string` | no |
| `address` | body | `string` | no |
| `address2` | body | `string` | no |
| `city` | body | `string` | no |
| `contact` | body | `string` | no |
| `countryRegionCode` | body | `string` | no |
| `county` | body | `string` | no |
| `email` | body | `string` | no |
| `faxNo` | body | `string` | no |
| `gln` | body | `string` | no |
| `lastDateModified` | body | `string` | no |
| `locationCode` | body | `string` | no |
| `name` | body | `string` | no |
| `name2` | body | `string` | no |
| `phoneNo` | body | `string` | no |
| `postCode` | body | `string` | no |
| `salespersonCode` | body | `string` | no |
| `satAddressId` | body | `string` | no |
| `shipmentMethodCode` | body | `string` | no |
| `shippingAgentCode` | body | `string` | no |
| `shippingAgentServiceCode` | body | `string` | no |
| `taxAreaCode` | body | `string` | no |
| `taxLiable` | body | `string` | no |
| `upsZone` | body | `string` | no |
