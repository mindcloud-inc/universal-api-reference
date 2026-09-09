# Cancel Inbound Shipment with Walmart

Cancel an inbound shipment order.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/fulfillment/inbound-shipments/:inboundOrderId`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Cancel Inbound Shipment](https://developer.walmart.com/global-marketplace/reference/cancelshipment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inboundOrderId` | path | `string` | yes | Unique ID identifying inbound shipment request. |
