# List Product Listings with Extensiv Order Manager

Retrieves product listings from Extensiv Order Manager.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/listings`
- **Base URL:** `https://api.skubana.com`
- **Official documentation:** [List Product Listings](https://documentation.skubana.com/pages/order-manager.html#tag/Listings/operation/getListingsUsingGET)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `active` | query | `boolean` | no |
| `createdDateFrom` | query | `string` | no |
| `createdDateTo` | query | `string` | no |
| `listingId[]` | query | `array<number>` | no |
| `listingSku[]` | query | `array<string>` | no |
| `masterSku[]` | query | `array<string>` | no |
| `modifiedDateFrom` | query | `string` | no |
| `modifiedDateTo` | query | `string` | no |
| `productId[]` | query | `array` | no |
| `salesChannelId` | query | `string` | no |
| `warehouseId` | query | `string` | no |
