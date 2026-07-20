# Add Vendor with ServiceTitan

## Endpoint

- **Method:** `POST`
- **Path:** `inventory/v2/tenant/{tenant}/vendors`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Add Vendor](https://developer.servicetitan.io/api-details/#api=tenant-inventory-v2&operation=Vendors_Create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address.street` | body | `string` | no | — |
| `externalData.applicationGuid` | body | `string` | no | — |
| `externalData.externalData[].key` | body | `string` | no | — |
| `name` | body | `string` | no | — |
| `tags[].tagTypeId` | body | `number` | no | — |
| `vendorContacts[].name` | body | `string` | no | — |
| `active` | body | `boolean` | no | Format: `toggle`. |
| `address.unit` | body | `string` | no | — |
| `externalData.externalData[]` | body | `array` | no | — |
| `externalData.externalData[].value` | body | `string` | no | — |
| `vendorContacts[].email` | body | `string` | no | — |
| `address.city` | body | `string` | no | — |
| `memo` | body | `string` | no | — |
| `address.state` | body | `string` | no | — |
| `firstName` | body | `string` | no | — |
| `address.zip` | body | `string` | no | — |
| `lastName` | body | `string` | no | — |
| `address.country` | body | `string` | no | — |
| `phone` | body | `string` | no | — |
| `email` | body | `string` | no | — |
| `fax` | body | `string` | no | — |
| `isTruckReplenishment` | body | `boolean` | no | Format: `toggle`. |
| `taxRate` | body | `number` | no | — |
| `restrictedMobileCreation` | body | `boolean` | no | Format: `toggle`. |
| `vendorQuickbooksItem` | body | `string` | no | — |
| `paymentTermId` | body | `number` | no | — |
| `remittanceVendorId` | body | `number` | no | — |
| `address` | body | `object` | no | — |
| `vendorContacts[]` | body | `array` | no | — |
| `externalData` | body | `object` | no | — |
| `deliveryOption` | body | `string` | no | — |
| `tags[]` | body | `array` | no | — |
