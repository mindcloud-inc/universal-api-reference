# List Inbound Shipments with Walmart

Retrieve a list of inbound shipments with optional filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/fulfillment/inbound-shipments`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [List Inbound Shipments](https://developer.walmart.com/us-marketplace/reference/getinboundshipments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inboundOrderId` | query | `string` | no | Unique ID identifying inbound shipment request. |
| `shipmentId` | query | `string` | no | Unique ID identifying each shipment. |
| `status` | query | `list<string>` | no | Current shipment status. |
| `fromCreateDate` | query | `date` | no | Shipment create date starting range.  Example: `2020-11-21T00:00:00.000Z` |
| `fromCreateDate_copy` | query | `date` | no | Shipment create date end range.  Example: `2020-11-22T00:00:00.000Z` |
