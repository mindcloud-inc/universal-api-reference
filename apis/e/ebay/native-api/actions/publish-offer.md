# Publish Offer with eBay

Convert an unpublished offer into a published offer (or live eBay listing).

## Endpoint

- **Method:** `POST`
- **Path:** `sell/inventory/v1/offer/:offerId/publish`
- **Base URL:** `https://api.ebay.com/`
- **API:** REST
- **Official documentation:** [Publish Offer](https://developer.ebay.com/api-docs/sell/inventory/resources/offer/methods/publishOffer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offerId` | path | `string` | yes | Specify the unique identifier of the offer that is to be published. Use the "List Offers by SKU" action to retrieve offer IDs. |
