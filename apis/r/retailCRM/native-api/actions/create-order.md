# Create Order with retailCRM

Creates a new order in retailCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/create`
- **Base URL:** `{accountUrl}/api/v5`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `site` | body | `list` | yes |
| `order.externalId` | body | `string` | yes |
| `order.firstName` | body | `string` | yes |
| `order.lastName` | body | `string` | no |
| `order.phone` | body | `string` | yes |
| `order.orderType` | body | `list` | yes |
| `order.orderMethod` | body | `list` | yes |
| `order.items[0].productName` | body | `string` | yes |
| `order.items[0].quantity` | body | `number` | yes |
| `order.items[0].initialPrice` | body | `number` | yes |
| `order.items[0].purchasePrice` | body | `number` | no |
