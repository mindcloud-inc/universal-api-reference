# Create Item Fulfilment with Rithum for Brands

Create Item fullfilment

## Endpoint

- **Method:** `POST`
- **Path:** `Fulfillments`
- **Base URL:** `https://api.channeladvisor.com/v1/`
- **Official documentation:** [Create Item Fulfilment](https://api.channeladvisor.com/apidocs#tag/Fulfillments/operation/Fulfillments.Fulfillment.CreateFulfillment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `deliveryStatus` | body | `string` | no |
| `TrackingNumber` | body | `string` | no |
| `distributionCenterID` | body | `number` | no |
| `insuranceCost` | body | `number` | no |
| `orderID` | body | `number` | no |
| `profileID` | body | `list<number>` | no |
| `returnTrackingNumber` | body | `string` | no |
| `sellerFulfillmentID` | body | `string` | no |
| `serialShippingContainerCode` | body | `string` | no |
| `shippedDateUtc` | body | `string` | no |
| `shippingCarrier` | body | `string` | no |
| `shippingClass` | body | `string` | no |
| `shippingCost` | body | `number` | no |
| `shippingLabelRequestID` | body | `string` | no |
| `stagingLocation` | body | `string` | no |
| `taxCost` | body | `number` | no |
| `trackingUrl` | body | `string` | no |
| `type` | body | `string` | no |
