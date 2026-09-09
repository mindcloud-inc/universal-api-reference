# Update Shipment Tracking with Walmart

Enter Carrier and Tracking information for shipments.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/fulfillment/shipment-tracking`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Update Shipment Tracking](https://developer.walmart.com/us-marketplace/reference/updateshipmenttrackingdetails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipmentID` | body | `string` | yes | — |
| `carrierName` | body | `string` | yes | — |
| `trackingInfo` | body | `string` | no | Maximum length: 100. Send multiple values as a array. |
