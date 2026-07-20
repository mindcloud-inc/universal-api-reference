# List Purchase Order Types with ServiceTitan

Retrieves purchase order types from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `inventory/v2/tenant/{tenant}/purchase-order-types`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [List Purchase Order Types](https://developer.servicetitan.io/api-details/#api=tenant-inventory-v2&operation=PurchaseOrderTypes_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `active` | query | `string` | no |
| `createdBefore` | query | `string` | no |
| `createdOnOrAfter` | query | `string` | no |
| `includeTotal` | query | `boolean` | no |
| `modifiedBefore` | query | `string` | no |
| `modifiedOnOrAfter` | query | `string` | no |
| `sort` | query | `string` | no |
