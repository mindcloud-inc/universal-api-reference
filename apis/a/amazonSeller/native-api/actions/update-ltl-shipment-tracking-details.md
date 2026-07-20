# Update LTL Shipment Tracking Details with Amazon Seller

Updates LTL shipment tracking details in Amazon Seller.

## Endpoint

- **Method:** `POST`
- **Path:** `inbound/fba/2024-03-20/inboundPlans/:inboundPlanId/shipments/:shipmentId/trackingDetails`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [Update LTL Shipment Tracking Details](https://developer-docs.amazon.com/sp-api/reference/updateshipmenttrackingdetails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inboundPlanId` | path | `string` | yes | Identifier of an inbound plan. |
| `shipmentId` | path | `string` | yes | Identifier of a shipment. A shipment contains the boxes and units being inbounded. |
| `freightBillNumber` | body | `string` | yes | Number associated with the freight bill. (required: 1 \| max: 1) Maximum length: 1. Send multiple values as a array. |
| `billOfLadingNumber` | body | `string` | no | The number of the carrier shipment acknowledgement document. (max length between 1 and 1024) |
