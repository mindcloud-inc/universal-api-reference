# Get Shipment Items by ID with Amazon Seller

Retrieves items from an Amazon Seller inbound shipment.

## Endpoint

- **Method:** `GET`
- **Path:** `fba/inbound/v0/shipments/:shipmentId/items`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** QueryType / NextToken
- **Official documentation:** [Get Shipment Items by ID](https://developer-docs.amazon.com/sp-api/reference/getorders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipmentId` | path | `string` | yes | A shipment identifier used for selecting items in a specific inbound shipment. |
