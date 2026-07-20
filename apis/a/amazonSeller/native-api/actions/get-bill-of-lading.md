# Get Bill of Lading with Amazon Seller

Retrieves a shipment bill of lading from Amazon Seller.

## Endpoint

- **Method:** `GET`
- **Path:** `fba/inbound/v0/shipments/:shipmentId/billOfLading`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [Get Bill of Lading](https://developer-docs.amazon.com/sp-api/reference/getbilloflading)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipmentId` | path | `string` | yes | A shipment identifier originally returned by the `Create Inbound ShipmentPlan` operation. |
