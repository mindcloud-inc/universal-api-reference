# Update Offer with eBay

Updates an offer for a specific inventory item on a specific eBay marketplace. It is up to the sellers whether they want to create a complete offer (with all necessary details) right from the start, or sellers can provide only some information with the initial createOffer call, and then make one or more subsequent updateOffer calls to complete the offer and prepare to publish the offer. Upon first creating an offer, the following fields are required in the request payload: sku, marketplaceId, and (listing) format.

## Endpoint

- **Method:** `PUT`
- **Path:** `sell/inventory/v1/offer/:offerId`
- **Base URL:** `https://api.ebay.com/`
- **API:** REST
- **Official documentation:** [Update Offer](https://developer.ebay.com/api-docs/sell/inventory/resources/offer/methods/updateOffer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listingPolicies.fulfillmentPolicyId` | body | `string` | no | This unique identifier indicates the fulfillment business policy that will be used once an offer is published and converted to an eBay listing. This fulfillment business policy will set all fulfillment-related settings for the eBay listing.  Business policies are not immediately required for offers, but are required before an offer can be published. The seller should review the fulfillment business policy before assigning it to the offer to make sure it is compatible with the inventory item and the offer settings. The seller may also want to review the shipping service costs in the fulfillment policy, and that seller might decide to override the shipping costs for one or more shipping service options by using the shippingCostOverrides container. |
| `pricingSummary.price.currency` | body | `string` | no | A three-digit string value representing the type of currency being used. Both the value and currency fields are required/always returned when expressing prices. |
| `sku` | body | `string` | yes | The seller-defined SKU value of the product that will be listed on the eBay site (specified in the marketplaceId field). Only one offer (in unpublished or published state) may exist for each sku/marketplaceId/format combination. This field is required. |
| `listingPolicies.returnPolicyId` | body | `string` | no | This unique identifier indicates the return business policy that will be used once an offer is published and converted to an eBay listing. This return business policy will set all return policy settings for the eBay listing. |
| `marketplaceId` | body | `list` | yes | This enumeration value is the unique identifier of the eBay site for which the offer will be made available. See MarketplaceEnum for the list of supported enumeration values. This field is required. |
| `pricingSummary.price.value` | body | `string` | no | A string representation of a dollar value expressed in the currency specified in the currency field. Both the value and currency fields are required/always returned when expressing prices. |
| `format` | body | `list` | yes | Indicates the listing format of the offer to be created in this request. Supported values are "FIXED_PRICE" or "AUCTION". |
| `listingPolicies.paymentPolicyId` | body | `string` | no | This unique identifier indicates the payment business policy that will be used once an offer is published and converted to an eBay listing. This payment business policy will set all payment-related settings for the eBay listing.  Business policies are not immediately required for offers, but are required before an offer can be published. The seller should review the payment business policy to make sure that it is compatible with the marketplace and listing category before assigning it to the offer. |
| `pricingSummary.price` | body | `object` | no | — |
| `categoryId` | body | `string` | no | The availableQuantity set here (in the offer) overrides the 'availability.shipToLocationAvailability.quantity' set in the inventory item. One of either quantity field is required before an offer can be published to create an active listing. An out of stock listing will result if set to 0. |
| `availableQuantity` | body | `number` | no | Quantity must be set to 1 or more in order for the inventory item to be purchasable, but this field is not necessarily required, even for published offers, if the general quantity of the inventory item has already been set in the inventory item record. |
| `merchantLocationKey` | body | `string` | no | The unique identifier of a merchant's inventory location (where the inventory item in the offer is located). This field is required before an offer can be published to create an active listing.  To get more information about inventory locations, the getInventoryLocations method can be used. |
| `listingDuration` | body | `list` | no | This field is required before an offer can be published to create an active listing, but for now it's optional. This field indicates the number of days that the listing will be active. For fixed-price listings, this value must be set to GTC, but auction listings support different listing durations.  The GTC (Good 'Til Cancelled) listings are automatically renewed each calendar month until the seller decides to end the listing.  Note: If the listing duration expires for an auction offer without a winning bidder, the listing then becomes available as a fixed-price offer and listing duration will be GTC (Good 'Til Cancelled). |
| `pricingSummary` | body | `object` | no | This container and its two child fields (currency and value) are required before an offer can be published to create an active listing. |
| `listingPolicies` | body | `object` | no | — |
| `offerId` | path | `string` | yes | The unique 'offerId' of the offer to be updated. |
