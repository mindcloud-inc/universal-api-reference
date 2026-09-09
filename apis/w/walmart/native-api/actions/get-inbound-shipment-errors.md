# Get Inbound Shipment Errors with Walmart

Retrieve a list of errors for an inbound shipment request.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/fulfillment/inbound-shipment-errors`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Get Inbound Shipment Errors](https://developer.walmart.com/us-marketplace/reference/getinboundshipmentitems)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inboundOrderId` | query | `string` | yes | Unique ID identifying inbound shipment request. |
