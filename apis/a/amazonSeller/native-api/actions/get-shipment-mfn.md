# Get Shipment ( MFN ) with Amazon Seller

Retrieves a merchant fulfillment shipment from Amazon Seller.

## Endpoint

- **Method:** `GET`
- **Path:** `mfn/v0/shipments/:shipmentId`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [Get Shipment ( MFN )](https://developer-docs.amazon.com/sp-api/reference/getshipments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ShipmentIdList` | path | `string` | yes | The Amazon-defined shipment identifier for the shipment. Maximum length: 999. Send multiple values as a array. |
