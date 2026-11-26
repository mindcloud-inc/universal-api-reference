# Withdraw Offer with eBay

End a single-variation listing

## Endpoint

- **Method:** `POST`
- **Path:** `sell/inventory/v1/offer/:offerId/withdraw`
- **Base URL:** `https://api.ebay.com/`
- **API:** REST
- **Official documentation:** [Withdraw Offer](https://developer.ebay.com/api-docs/sell/inventory/resources/offer/methods/withdrawOffer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offerId` | path | `string` | yes | The ID of an Offer to withdraw. |
