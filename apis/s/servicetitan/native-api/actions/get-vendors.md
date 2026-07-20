# List Vendors with ServiceTitan

Retrieves vendors from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `inventory/v2/tenant/{tenant}/vendors`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [List Vendors](https://developer.servicetitan.io/api-details/#api=tenant-inventory-v2&operation=Vendors_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ids` | query | `string` | no |
| `active` | query | `string` | no |
| `createdBefore` | query | `string` | no |
| `createdOnOrAfter` | query | `string` | no |
| `externalDataApplicationGuid` | query | `string` | no |
| `externalDataKey` | query | `string` | no |
| `externalDataValues` | query | `string` | no |
| `includeTotal` | query | `boolean` | no |
| `modifiedBefore` | query | `string` | no |
| `modifiedOnOrAfter` | query | `string` | no |
| `sort` | query | `string` | no |
