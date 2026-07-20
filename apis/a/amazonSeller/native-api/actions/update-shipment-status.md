# Update Shipment Status with Amazon Seller

Updates shipment status for an Amazon Seller order.

## Endpoint

- **Method:** `POST`
- **Path:** `orders/v0/orders/:orderId/shipment`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [Update Shipment Status](https://developer-docs.amazon.com/sp-api/reference/updateshipmentstatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MarketplaceId` | body | `list<string>` | yes | A marketplace identifier. Specifies the marketplace where the product would be stored. |
| `orderItems[].orderItemId` | body | `string` | no | The order item's unique identifier. |
| `orderId` | path | `string` | yes | An Amazon-defined order identifier, in 3-7-7 format. |
| `orderItems[].quantity` | body | `number` | no | The quantity for which to update the shipment status. |
| `shipmentStatus` | body | `list<string>` | yes | The shipment status to apply. |
| `orderItems[]` | body | `array<object>` | no | For partial shipment status updates, provide a list of order items and quantities to be updated. Leave blank to apply the new status to the entire order. |
