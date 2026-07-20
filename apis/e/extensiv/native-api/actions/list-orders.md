# List Orders with Extensiv Order Manager

Retrieves orders from Extensiv Order Manager.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.1/orders`
- **Base URL:** `https://api.skubana.com`
- **Official documentation:** [List Orders](https://documentation.skubana.com/pages/order-manager.html#tag/Order/operation/getOrdersUsingGET_1)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `createdDateFrom` | query | `string` | no | — |
| `createdDateTo` | query | `string` | no | — |
| `external` | query | `boolean` | no | — |
| `modifiedDateFrom` | query | `string` | no | — |
| `modifiedDateTo` | query | `string` | no | — |
| `orderDateFrom` | query | `string` | no | — |
| `orderDateTo` | query | `string` | no | — |
| `orderId` | query | `number` | no | — |
| `orderNumber[]` | query | `array<string>` | no | — |
| `paymentDateFrom` | query | `string` | no | — |
| `paymentDateTo` | query | `string` | no | — |
| `productId[]` | query | `array<number>` | no | — |
| `salesChannelId` | query | `number` | no | — |
| `shipDateFrom` | query | `string` | no | — |
| `shipDateTo` | query | `string` | no | — |
| `status` | query | `list<string>` | no | Send multiple values as a array. |
| `unresolvedStatus` | query | `list<string>` | no | Send multiple values as a array. |
| `warehouseId` | query | `number` | no | — |
