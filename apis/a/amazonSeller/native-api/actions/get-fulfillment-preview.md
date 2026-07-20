# Get Fulfillment Preview with Amazon Seller

Retrieves fulfillment order previews from Amazon Seller.

## Endpoint

- **Method:** `POST`
- **Path:** `https://sellingpartnerapi-na.amazon.com/fba/outbound/2020-07-01/fulfillmentOrders/preview`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [Get Fulfillment Preview](https://developer-docs.amazon.com/sp-api/reference/confirmshipment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `marketplaceId` | body | `string` | no | A marketplace identifier. Specifies the marketplace where the product would be stored. |
| `address.name` | body | `string` | yes | — |
| `items[].perUnitDeclaredValue[].currencyCode` | body | `string` | yes | Three digit currency code in ISO 4217 format. |
| `items[].sellerSku` | body | `string` | yes | — |
| `address` | body | `object` | yes | — |
| `address.addressLine1` | body | `string` | yes | — |
| `items[].perUnitDeclaredValue[].value` | body | `string` | yes | A decimal number with no loss of precision. Useful when precision loss is unacceptable, as with currencies. Follows RFC7159 for number representation. |
| `items[].quantity` | body | `number` | yes | — |
| `address.addressLine2` | body | `string` | no | — |
| `items[]` | body | `array` | no | — |
| `items[].sellerFulfillmentOrderItemId` | body | `string` | yes | A fulfillment order item identifier that the seller creates to track items in the fulfillment preview. |
| `address.addressLine3` | body | `string` | no | — |
| `includeCODFulfillmentPreview` | body | `boolean` | no | — |
| `items[].perUnitDeclaredValue[]` | body | `array` | no | — |
| `address.postalCode` | body | `string` | yes | — |
| `includeDeliveryWindows` | body | `boolean` | no | — |
| `address.countryCode` | body | `string` | yes | The two digit country code. In ISO 3166-1 alpha-2 format. |
| `shippingSpeedCategories[]` | body | `array` | no | — |
| `address.city` | body | `string` | yes | — |
| `address.districtOrCounty` | body | `string` | no | — |
| `address.stateOrRegion` | body | `string` | no | — |
| `address.phone` | body | `string` | no | — |
