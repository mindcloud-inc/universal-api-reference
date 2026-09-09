# Get Inbound Shipment Items with Walmart

Retrieve a list of inbound shipments with optional filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/fulfillment/inbound-shipment-items`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Get Inbound Shipment Items](https://developer.walmart.com/us-marketplace/reference/getinboundshipmentitems)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipmentId` | query | `string` | yes | Unique ID identifying each shipment. |
