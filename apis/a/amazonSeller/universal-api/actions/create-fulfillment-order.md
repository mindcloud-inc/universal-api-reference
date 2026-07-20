# Amazon Seller: Create Fulfillment Order

Creates a fulfillment order in Amazon Seller.

```
POST https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/create-fulfillment-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/create-fulfillment-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deliveryPreferences[].dropOffLocation[].type": "string",
  "destinationAddress.name": "Ava Chen",
  "items[].perUnitDeclaredValue[].currencyCode": "string",
  "items[].perUnitPrice[].currencyCode": "string",
  "items[].perUnitTax[].currencyCode": "string",
  "items[].sellerSku": "string",
  "paymentInformation[].paymentTransactionId": "string",
  "destinationAddress": {},
  "destinationAddress.addressLine1": "string",
  "items[].perUnitDeclaredValue[].value": "string",
  "items[].perUnitPrice[].value": "string",
  "items[].perUnitTax[].value": "string",
  "items[].quantity": 1,
  "paymentInformation[].paymentMode": "string",
  "paymentInformation[].paymentDate": "2026-05-07T12:00:00.000Z",
  "items[].sellerFulfillmentOrderItemId": "string",
  "sellerFulfillmentOrderId": "string",
  "destinationAddress.postalCode": "string",
  "displayableOrderId": "string",
  "destinationAddress.countryCode": "string",
  "displayableOrderDate": "string",
  "destinationAddress.city": "string",
  "displayableOrderComment": "string",
  "shippingSpeedCategory": "Standard"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/create-fulfillment-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deliveryPreferences[].dropOffLocation[].type": "string",
    "destinationAddress.name": "Ava Chen",
    "items[].perUnitDeclaredValue[].currencyCode": "string",
    "items[].perUnitPrice[].currencyCode": "string",
    "items[].perUnitTax[].currencyCode": "string",
    "items[].sellerSku": "string",
    "paymentInformation[].paymentTransactionId": "string",
    "destinationAddress": {},
    "destinationAddress.addressLine1": "string",
    "items[].perUnitDeclaredValue[].value": "string",
    "items[].perUnitPrice[].value": "string",
    "items[].perUnitTax[].value": "string",
    "items[].quantity": 1,
    "paymentInformation[].paymentMode": "string",
    "paymentInformation[].paymentDate": "2026-05-07T12:00:00.000Z",
    "items[].sellerFulfillmentOrderItemId": "string",
    "sellerFulfillmentOrderId": "string",
    "destinationAddress.postalCode": "string",
    "displayableOrderId": "string",
    "destinationAddress.countryCode": "string",
    "displayableOrderDate": "string",
    "destinationAddress.city": "string",
    "displayableOrderComment": "string",
    "shippingSpeedCategory": "Standard"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deliveryPreferences[].deliveryInstructions` | string | no | Additional delivery instructions. For example, this could be instructions on how to enter a building, nearby landmark or navigation instructions, or Beware of dogs. |
| `deliveryPreferences[].dropOffLocation[].type` | list | yes |  |
| `deliveryWindow[].startDate` | date | no | Date timestamp |
| `destinationAddress.name` | string | yes |  |
| `items[].perUnitDeclaredValue[].currencyCode` | string | yes | Three digit currency code in ISO 4217 format. |
| `items[].perUnitPrice[].currencyCode` | string | yes | Three digit currency code in ISO 4217 format. |
| `items[].perUnitTax[].currencyCode` | string | yes | Three digit currency code in ISO 4217 format. |
| `items[].sellerSku` | string | yes |  |
| `marketplaceId` | string | no | A marketplace identifier. Specifies the marketplace where the product would be stored. |
| `paymentInformation[].paymentTransactionId` | string | yes | The transaction identifier of this payment. |
| `deliveryPreferences[].dropOffLocation[]` | array | no |  |
| `deliveryWindow[].endDate` | date | no | Date timestamp |
| `destinationAddress` | object | yes |  |
| `destinationAddress.addressLine1` | string | yes |  |
| `items[].perUnitDeclaredValue[].value` | string | yes | A decimal number with no loss of precision. Useful when precision loss is unacceptable, as with currencies. Follows RFC7159 for number representation. |
| `items[].perUnitPrice[].value` | string | yes | A decimal number with no loss of precision. Useful when precision loss is unacceptable, as with currencies. Follows RFC7159 for number representation. |
| `items[].perUnitTax[].value` | string | yes | A decimal number with no loss of precision. Useful when precision loss is unacceptable, as with currencies. Follows RFC7159 for number representation. |
| `items[].quantity` | number | yes |  |
| `paymentInformation[].paymentMode` | string | yes | The transaction mode of this payment. |
| `destinationAddress.addressLine2` | string | no |  |
| `items[]` | array | no |  |
| `items[].perUnitDeclaredValue[]` | array | no |  |
| `paymentInformation[].paymentDate` | date | yes |  |
| `destinationAddress.addressLine3` | string | no |  |
| `items[].sellerFulfillmentOrderItemId` | string | yes | A fulfillment order item identifier that the seller creates to track fulfillment order items. Used to disambiguate multiple fulfillment items that have the same sellerSku value. For example, the seller might assign different sellerFulfillmentOrderItemId values to two items in a fulfillment order that share the same sellerSku value but have different giftMessage values. |
| `sellerFulfillmentOrderId` | string | yes | A fulfillment order identifier that the seller creates to track their fulfillment order. The sellerFulfillmentOrderId must be unique for each fulfillment order that a seller creates. If the seller's system already creates unique order identifiers, then these might be good values for them to use. |
| `destinationAddress.postalCode` | string | yes |  |
| `displayableOrderId` | string | yes | A fulfillment order identifier that the seller creates. This value displays as the order identifier in recipient-facing materials such as the outbound shipment packing slip. The value of displayableOrderId should match the order identifier that the seller provides to the recipient. The seller can use the SellerFulfillmentOrderId for this value or they can specify an alternate value if they want the recipient to reference an alternate order identifier. The value must be an alpha-numeric or ISO 8859-1 compliant string from one to 40 characters in length. Cannot contain two spaces in a row. Leading and trailing white space is removed. |
| `items[].giftMessage` | string | no | A message to the gift recipient, if applicable. |
| `destinationAddress.countryCode` | string | yes | The two digit country code. In ISO 3166-1 alpha-2 format. |
| `displayableOrderDate` | string | yes | Date timestamp |
| `items[].displayableComment` | string | no | Item-specific text that displays in recipient-facing materials such as the outbound shipment packing slip. |
| `destinationAddress.city` | string | yes |  |
| `displayableOrderComment` | string | yes | Order-specific text that appears in recipient-facing materials such as the outbound shipment packing slip. |
| `items[].fulfillmentNetworkSku` | string | no | Amazon's fulfillment network SKU of the item. |
| `destinationAddress.districtOrCounty` | string | no |  |
| `items[].perUnitPrice[]` | array | no |  |
| `shippingSpeedCategory` | list<string> | yes | The shipping method used for the fulfillment order. When this value is ScheduledDelivery, choose Ship for the fulfillmentAction. Hold is not a valid fulfillmentAction value when the shippingSpeedCategory value is ScheduledDelivery. Note: Shipping method service level agreements vary by marketplace. Sellers should refer to the Seller Central website in their marketplace for shipping method service level agreements and fulfillment fees. Default: `Standard`. |
| `deliveryWindow[]` | array | no |  |
| `destinationAddress.stateOrRegion` | string | no |  |
| `items[].perUnitTax[]` | array | no | An amount of money, including units in the form of currency. |
| `deliveryPreferences[]` | array | no |  |
| `destinationAddress.phone` | string | no |  |
| `fulfillmentAction` | list<string> | no |  |
| `fulfillmentPolicy` | string | no |  |
| `codSettings[]` | array | no | The COD (Cash On Delivery) charges that you associate with a COD fulfillment order. |
| `shipFromCountryCode` | string | no |  |
| `notificationEmails[]` | array | no | A list of email addresses that the seller provides that are used by Amazon to send ship-complete notifications to recipients on behalf of the seller. |
| `featureConstraints[]` | array | no |  |
| `paymentInformation[]` | array | no | An array of various payment attributes related to this fulfillment order. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Amazon Seller API returns.

## Native endpoint

Through the native Amazon Seller API, this operation is `POST https://sellingpartnerapi-na.amazon.com/fba/outbound/2020-07-01/fulfillmentOrders` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-fulfillment-order.md) for the provider-specific parameters and requirements.

