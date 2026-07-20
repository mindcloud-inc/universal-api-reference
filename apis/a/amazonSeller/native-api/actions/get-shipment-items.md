# List Shipment Items with Amazon Seller

Retrieves inbound shipment items from Amazon Seller.

## Endpoint

- **Method:** `GET`
- **Path:** `fba/inbound/v0/shipmentItems`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** QueryType / NextToken
- **Official documentation:** [List Shipment Items](https://developer-docs.amazon.com/sp-api/reference/getshipmentitems)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MarketplaceId` | query | `list<string>` | yes | A marketplace identifier. Specifies the marketplace where the product would be stored. |
| `LastUpdatedAfter` | query | `string` | no | A date used for selecting inbound shipment items that were last updated after (or at) a specified time. The selection includes updates made by Amazon and by the seller. |
| `LastUpdatedBefore` | query | `string` | no | A date used for selecting inbound shipment items that were last updated before (or at) a specified time. The selection includes updates made by Amazon and by the seller. |
