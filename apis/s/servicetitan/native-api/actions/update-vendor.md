# Update Vendor with ServiceTitan

## Endpoint

- **Method:** `PATCH`
- **Path:** `inventory/v2/tenant/{tenant}/vendors/:id`
- **Base URL:** `https://{baseUrl}/`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `address.street` | body | `string` | no |
| `externalData.applicationGuid` | body | `string` | no |
| `externalData.externalData[].value` | body | `string` | no |
| `name` | body | `string` | no |
| `vendorContacts[].name` | body | `string` | no |
| `active` | body | `boolean` | no |
| `address.unit` | body | `string` | no |
| `externalData.externalData[].key` | body | `string` | no |
| `externalData.patchMode` | body | `object` | no |
| `vendorContacts[].email` | body | `string` | no |
| `address.city` | body | `string` | no |
| `externalData.externalData[]` | body | `array` | no |
| `memo` | body | `string` | no |
| `address.state` | body | `string` | no |
| `firstName` | body | `string` | no |
| `address.zip` | body | `string` | no |
| `lastName` | body | `string` | no |
| `address.country` | body | `string` | no |
| `phone` | body | `string` | no |
| `email` | body | `string` | no |
| `fax` | body | `string` | no |
| `externalData` | body | `object` | no |
| `isTruckReplenishment` | body | `string` | no |
| `taxRate` | body | `number` | no |
| `restrictedMobileCreation` | body | `boolean` | no |
| `vendorQuickbooksItem` | body | `string` | no |
| `paymentTermId` | body | `number` | no |
| `remittanceVendorId` | body | `number` | no |
| `address` | body | `object` | no |
| `id` | path | `string` | no |
| `vendorContacts[]` | body | `array` | no |
