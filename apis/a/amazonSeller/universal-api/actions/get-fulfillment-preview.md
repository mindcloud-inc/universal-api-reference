# Amazon Seller: Get Fulfillment Preview

Retrieves fulfillment order previews from Amazon Seller.

```
POST https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-fulfillment-preview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-fulfillment-preview" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address.name": "Ava Chen",
  "items[].perUnitDeclaredValue[].currencyCode": "string",
  "items[].sellerSku": "string",
  "address": {},
  "address.addressLine1": "string",
  "items[].perUnitDeclaredValue[].value": "string",
  "items[].quantity": 1,
  "items[].sellerFulfillmentOrderItemId": "string",
  "address.postalCode": "string",
  "address.countryCode": "string",
  "address.city": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-fulfillment-preview', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address.name": "Ava Chen",
    "items[].perUnitDeclaredValue[].currencyCode": "string",
    "items[].sellerSku": "string",
    "address": {},
    "address.addressLine1": "string",
    "items[].perUnitDeclaredValue[].value": "string",
    "items[].quantity": 1,
    "items[].sellerFulfillmentOrderItemId": "string",
    "address.postalCode": "string",
    "address.countryCode": "string",
    "address.city": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `marketplaceId` | string | no | A marketplace identifier. Specifies the marketplace where the product would be stored. |
| `address.name` | string | yes |  |
| `items[].perUnitDeclaredValue[].currencyCode` | string | yes | Three digit currency code in ISO 4217 format. |
| `items[].sellerSku` | string | yes |  |
| `address` | object | yes |  |
| `address.addressLine1` | string | yes |  |
| `items[].perUnitDeclaredValue[].value` | string | yes | A decimal number with no loss of precision. Useful when precision loss is unacceptable, as with currencies. Follows RFC7159 for number representation. |
| `items[].quantity` | number | yes |  |
| `address.addressLine2` | string | no |  |
| `items[]` | array | no |  |
| `items[].sellerFulfillmentOrderItemId` | string | yes | A fulfillment order item identifier that the seller creates to track items in the fulfillment preview. |
| `address.addressLine3` | string | no |  |
| `includeCODFulfillmentPreview` | boolean | no |  |
| `items[].perUnitDeclaredValue[]` | array | no |  |
| `address.postalCode` | string | yes |  |
| `includeDeliveryWindows` | boolean | no |  |
| `address.countryCode` | string | yes | The two digit country code. In ISO 3166-1 alpha-2 format. |
| `shippingSpeedCategories[]` | array | no |  |
| `address.city` | string | yes |  |
| `address.districtOrCounty` | string | no |  |
| `address.stateOrRegion` | string | no |  |
| `address.phone` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Amazon Seller API returns.

## Native endpoint

Through the native Amazon Seller API, this operation is `POST https://sellingpartnerapi-na.amazon.com/fba/outbound/2020-07-01/fulfillmentOrders/preview` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fulfillment-preview.md) for the provider-specific parameters and requirements.

