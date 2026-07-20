# Fulfill Order with SquareSpace

Updates order fulfillments in Squarespace.

## Endpoint

- **Method:** `POST`
- **Path:** `/1.0/commerce/orders/:id/fulfillments`
- **Base URL:** `https://api.squarespace.com`
- **Official documentation:** [Fulfill Order](https://developers.squarespace.com/commerce-apis/orders#fulfill-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `list<string>` | yes | Order ID to fulfill. |
| `shipments[]` | body | `array<object>` | yes | List of shipment payload objects. |
| `shipments[].carrierName` | body | `string` | yes | Carrier name. |
| `shipments[].service` | body | `string` | yes | Carrier service level. |
| `shipments[].shipDate` | body | `string` | yes | Shipment datetime in ISO 8601 UTC. |
| `shipments[].trackingNumber` | body | `string` | yes | Parcel tracking number. |
| `shipments[].trackingUrl` | body | `string` | no | Carrier tracking URL. |
| `shouldSendNotification` | body | `boolean` | no | Send shipment email notification to customer. |
