# List Shipments with Amazon Seller

Retrieves inbound shipments from Amazon Seller.

## Endpoint

- **Method:** `GET`
- **Path:** `fba/inbound/v0/shipments`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** QueryType / NextToken
- **Official documentation:** [List Shipments](https://developer-docs.amazon.com/sp-api/reference/getshipments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `QueryType` | query | `list<string>` | yes | Select how you want to look up shipments. You can search by specific IDs/Statuses or a Date Range. |
| `MarketplaceId` | query | `list<string>` | yes | A marketplace identifier. Specifies the marketplace where the product would be stored. |
| `ShipmentStatusList` | query | `list<string>` | no | Return inbound shipments with a current status that matches the status values you specify. - WORKING	The shipment was created by the seller, but has not yet shipped. - READY_TO_SHIP	The seller has printed box labels (for Small parcel shipments) or pallet labels (for Less Than Truckload shipments). - SHIPPED	The shipment was picked up by the carrier. - RECEIVING	The shipment has arrived at the fulfillment center, but not all items have been marked as received. - CANCELLED	The shipment was cancelled by the seller after the shipment was sent to the fulfillment center. - DELETED	The shipment was cancelled by the seller before the shipment was sent to the fulfillment center. - CLOSED	The shipment has arrived at the fulfillment center and all items have been marked as received. - ERROR	There was an error with the shipment and it was not processed by Amazon. - IN_TRANSIT	The carrier has notified the fulfillment center that it is aware of the shipment. - DELIVERED	The shipment was delivered by the carrier to the fulfillment center. - CHECKED_IN	The shipment was checked-in at the receiving dock of the fulfillment center. Send multiple values as a array. |
| `ShipmentIdList` | query | `string` | no | A list of shipment IDs used to select the shipments that you want.  If both `ShipmentStatusList` and `ShipmentIdList` are specified, only shipments that match both parameters are returned.  Array of strings, max length: `999` Maximum length: 999. Send multiple values as a array. |
| `LastUpdatedAfter` | query | `string` | no | A date used for selecting inbound shipments that were last updated after (or at) a specified time. The selection includes updates made by Amazon and by the seller. |
| `LastUpdatedBefore` | query | `string` | no | A date used for selecting inbound shipments that were last updated before (or at) a specified time. The selection includes updates made by Amazon and by the seller. |
