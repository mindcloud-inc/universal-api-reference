# Create Fulfillment Order with Amazon Seller

Creates a fulfillment order in Amazon Seller.

## Endpoint

- **Method:** `POST`
- **Path:** `https://sellingpartnerapi-na.amazon.com/fba/outbound/2020-07-01/fulfillmentOrders`
- **Base URL:** `https://{environment}-{region}.amazon.com`
- **API:** REST
- **Official documentation:** [Create Fulfillment Order](https://developer-docs.amazon.com/sp-api/reference/confirmshipment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deliveryPreferences[].deliveryInstructions` | body | `string` | no | Additional delivery instructions. For example, this could be instructions on how to enter a building, nearby landmark or navigation instructions, or Beware of dogs. |
| `deliveryPreferences[].dropOffLocation[].type` | body | `list` | yes | — |
| `deliveryWindow[].startDate` | body | `date` | no | Date timestamp |
| `destinationAddress.name` | body | `string` | yes | — |
| `items[].perUnitDeclaredValue[].currencyCode` | body | `string` | yes | Three digit currency code in ISO 4217 format. |
| `items[].perUnitPrice[].currencyCode` | body | `string` | yes | Three digit currency code in ISO 4217 format. |
| `items[].perUnitTax[].currencyCode` | body | `string` | yes | Three digit currency code in ISO 4217 format. |
| `items[].sellerSku` | body | `string` | yes | — |
| `marketplaceId` | body | `string` | no | A marketplace identifier. Specifies the marketplace where the product would be stored. |
| `paymentInformation[].paymentTransactionId` | body | `string` | yes | The transaction identifier of this payment. |
| `deliveryPreferences[].dropOffLocation[]` | body | `array` | no | — |
| `deliveryWindow[].endDate` | body | `date` | no | Date timestamp |
| `destinationAddress` | body | `object` | yes | — |
| `destinationAddress.addressLine1` | body | `string` | yes | — |
| `items[].perUnitDeclaredValue[].value` | body | `string` | yes | A decimal number with no loss of precision. Useful when precision loss is unacceptable, as with currencies. Follows RFC7159 for number representation. |
| `items[].perUnitPrice[].value` | body | `string` | yes | A decimal number with no loss of precision. Useful when precision loss is unacceptable, as with currencies. Follows RFC7159 for number representation. |
| `items[].perUnitTax[].value` | body | `string` | yes | A decimal number with no loss of precision. Useful when precision loss is unacceptable, as with currencies. Follows RFC7159 for number representation. |
| `items[].quantity` | body | `number` | yes | — |
| `paymentInformation[].paymentMode` | body | `string` | yes | The transaction mode of this payment. |
| `destinationAddress.addressLine2` | body | `string` | no | — |
| `items[]` | body | `array` | no | — |
| `items[].perUnitDeclaredValue[]` | body | `array` | no | — |
| `paymentInformation[].paymentDate` | body | `date` | yes | — |
| `destinationAddress.addressLine3` | body | `string` | no | — |
| `items[].sellerFulfillmentOrderItemId` | body | `string` | yes | A fulfillment order item identifier that the seller creates to track fulfillment order items. Used to disambiguate multiple fulfillment items that have the same sellerSku value. For example, the seller might assign different sellerFulfillmentOrderItemId values to two items in a fulfillment order that share the same sellerSku value but have different giftMessage values. |
| `sellerFulfillmentOrderId` | body | `string` | yes | A fulfillment order identifier that the seller creates to track their fulfillment order. The sellerFulfillmentOrderId must be unique for each fulfillment order that a seller creates. If the seller's system already creates unique order identifiers, then these might be good values for them to use. |
| `destinationAddress.postalCode` | body | `string` | yes | — |
| `displayableOrderId` | body | `string` | yes | A fulfillment order identifier that the seller creates. This value displays as the order identifier in recipient-facing materials such as the outbound shipment packing slip. The value of displayableOrderId should match the order identifier that the seller provides to the recipient. The seller can use the SellerFulfillmentOrderId for this value or they can specify an alternate value if they want the recipient to reference an alternate order identifier.  The value must be an alpha-numeric or ISO 8859-1 compliant string from one to 40 characters in length. Cannot contain two spaces in a row. Leading and trailing white space is removed. |
| `items[].giftMessage` | body | `string` | no | A message to the gift recipient, if applicable. |
| `destinationAddress.countryCode` | body | `string` | yes | The two digit country code. In ISO 3166-1 alpha-2 format. |
| `displayableOrderDate` | body | `string` | yes | Date timestamp |
| `items[].displayableComment` | body | `string` | no | Item-specific text that displays in recipient-facing materials such as the outbound shipment packing slip. |
| `destinationAddress.city` | body | `string` | yes | — |
| `displayableOrderComment` | body | `string` | yes | Order-specific text that appears in recipient-facing materials such as the outbound shipment packing slip. |
| `items[].fulfillmentNetworkSku` | body | `string` | no | Amazon's fulfillment network SKU of the item. |
| `destinationAddress.districtOrCounty` | body | `string` | no | — |
| `items[].perUnitPrice[]` | body | `array` | no | — |
| `shippingSpeedCategory` | body | `list<string>` | yes | The shipping method used for the fulfillment order. When this value is ScheduledDelivery, choose Ship for the fulfillmentAction. Hold is not a valid fulfillmentAction value when the shippingSpeedCategory value is ScheduledDelivery. Note: Shipping method service level agreements vary by marketplace. Sellers should refer to the Seller Central website in their marketplace for shipping method service level agreements and fulfillment fees. |
| `deliveryWindow[]` | body | `array` | no | — |
| `destinationAddress.stateOrRegion` | body | `string` | no | — |
| `items[].perUnitTax[]` | body | `array` | no | An amount of money, including units in the form of currency. |
| `deliveryPreferences[]` | body | `array` | no | — |
| `destinationAddress.phone` | body | `string` | no | — |
| `fulfillmentAction` | body | `list<string>` | no | — |
| `fulfillmentPolicy` | body | `string` | no | — |
| `codSettings[]` | body | `array` | no | The COD (Cash On Delivery) charges that you associate with a COD fulfillment order. |
| `shipFromCountryCode` | body | `string` | no | — |
| `notificationEmails[]` | body | `array` | no | A list of email addresses that the seller provides that are used by Amazon to send ship-complete notifications to recipients on behalf of the seller. |
| `featureConstraints[]` | body | `array` | no | — |
| `paymentInformation[]` | body | `array` | no | An array of various payment attributes related to this fulfillment order. |
