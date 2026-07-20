# Cancel Shipment with Amazon Seller

Cancels a merchant fulfillment shipment in Amazon Seller.

## Endpoint

- **Method:** `DELETE`
- **Path:** `mfn/v0/shipments/:shipmentId`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [Cancel Shipment](https://developer-docs.amazon.com/sp-api/reference/cancelshipment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `shipmentId` | path | `string` | yes |
