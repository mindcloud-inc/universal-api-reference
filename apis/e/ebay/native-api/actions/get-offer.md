# Get Offer with eBay

Retrieve an Offer by it's unique offer ID.

## Endpoint

- **Method:** `GET`
- **Path:** `sell/inventory/v1/offer/:offerID`
- **Base URL:** `https://api.ebay.com/`
- **API:** REST
- **Official documentation:** [Get Offer](https://developer.ebay.com/api-docs/sell/inventory/resources/offer/methods/getOffer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offerID` | path | `string` | yes | The unique ID of an offer to retrieve. Use the "List Offers by SKU" action to retrieve offer IDs. |
