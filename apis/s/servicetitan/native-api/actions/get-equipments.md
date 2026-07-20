# Get Equipments with ServiceTitan

Retrieves pricebook equipment from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `pricebook/v2/tenant/{tenant}/equipment`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Equipments](https://developer.servicetitan.io/api-details/#api=tenant-pricebook-v2&operation=Equipment_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `modifiedOnOrAfter` | query | `string` | no |
| `createdOnOrAfter` | query | `string` | no |
