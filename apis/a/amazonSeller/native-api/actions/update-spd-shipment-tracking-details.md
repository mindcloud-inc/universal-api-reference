# Update SPD Shipment Tracking Details with Amazon Seller

Updates SPD shipment tracking details in Amazon Seller.

## Endpoint

- **Method:** `POST`
- **Path:** `inbound/fba/2024-03-20/inboundPlans/:inboundPlanId/shipments/:shipmentId/trackingDetails`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [Update SPD Shipment Tracking Details](https://developer-docs.amazon.com/sp-api/reference/updateshipmenttrackingdetails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inboundPlanId` | path | `string` | yes | Identifier of an inbound plan. |
| `ltlTrackingDetail.billOfLadingNumber` | body | `string` | no | The number of the carrier shipment acknowledgement document. (max length between 1 and 1024) |
| `shipmentId` | path | `string` | yes | Identifier of a shipment. A shipment contains the boxes and units being inbounded. |
| `spdTrackingItems[]` | body | `array<object>` | no | List of Small Parcel Delivery (SPD) tracking items. |
| `spdTrackingItems[].boxId` | body | `string` | no | The ID provided by Amazon that identifies a given box. This ID is comprised of the external shipment ID (which is generated after transportation has been confirmed) and the index of the box. |
| `ltlTrackingDetail` | body | `object` | no | Contains input information to update Less-Than-Truckload (LTL) tracking information. |
| `ltlTrackingDetail.freightBillNumber` | body | `string` | no | (required when shipping LTL) Number associated with the freight bill. Maximum length: 1. Send multiple values as a array. |
| `spdTrackingItems[].trackingID` | body | `string` | no | The tracking ID associated with each box in a non-Amazon partnered Small Parcel Delivery (SPD) shipment. The seller must provide this information. |
