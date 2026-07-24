# List Sales with Cin7 Core

## Endpoint

- **Method:** `GET`
- **Path:** `saleList`
- **Base URL:** `https://inventory.dearsystems.com/externalapi/v2/`
- **Official documentation:** [List Sales](https://dearinventory.docs.apiary.io/#reference/sale/sale-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Search` | query | `string` | no |
| `CreatedSince` | query | `string` | no |
| `UpdatedSince` | query | `string` | no |
| `OrderStatus` | query | `string` | no |
| `ExternalID` | query | `string` | no |
| `Status` | query | `string` | no |
| `OrderLocationID` | query | `string` | no |
| `CombinedPickStatus` | query | `string` | no |
| `Status` | query | `string` | no |
