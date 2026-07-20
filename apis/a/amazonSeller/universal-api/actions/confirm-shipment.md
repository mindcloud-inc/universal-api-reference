# Amazon Seller: Confirm Shipment

Updates shipment confirmation for an Amazon Seller order.

```
PUT https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/confirm-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/confirm-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": "string",
  "marketplaceId": "string",
  "packageReferenceId": "string",
  "shipDate": "string",
  "carrierCode": "string",
  "trackingNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/confirm-shipment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": "string",
    "marketplaceId": "string",
    "packageReferenceId": "string",
    "shipDate": "string",
    "carrierCode": "string",
    "trackingNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | string | yes | An Amazon-defined order identifier, in 3-7-7 format. |
| `marketplaceId` | list<string> | yes | A marketplace identifier. Specifies the marketplace where the product would be stored. |
| `orderItems[].orderItemId` | string | no | *required* The order item's unique identifier. |
| `orderItems[].quantity` | string | no | The items quantity. |
| `packageReferenceId` | string | yes | A seller-supplied identifier that uniquely identifies a package within the scope of an order. Only positive numeric values are supported. |
| `orderItems[].transparencyCodes` | string | no | A list of order items. (array of strings) Accepts multiple values as an array. |
| `shipDate` | string | yes | The shipping date for the package. Must be in ISO 8601 date/time format. |
| `carrierCode` | string | yes | Identifies the carrier that will deliver the package. This field is required for all marketplaces. For more information, refer to the (Carrier Code announcement)[https://developer-docs.amazon.com/sp-api/changelog/carriercode-value-required-in-shipment-confirmations-for-br-mx-ca-sg-au-in-jp-marketplaces] |
| `carrierName` | string | no | Carrier name that will deliver the package. Required when carrierCode is "Other" |
| `trackingNumber` | string | yes | The tracking number used to obtain tracking and delivery information. |
| `orderItems[]` | array<object> | no | A list of order items. |
| `shippingMethod` | string | no | Ship method to be used for shipping the order. |
| `shipFromSupplySourceId` | string | no | The unique identifier for the supply source. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `codCollectionMethod` | list<string> | no | The COD collection method (only supported in the JP marketplace). Allowed: `DirectPayment` |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orderId": "string",
      "packageReferenceId": "string",
      "shipDate": "string",
      "trackingNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orderId` | string | Confirmed Amazon order identifier. |
| `packageReferenceId` | string | Confirmed package reference identifier. |
| `shipDate` | string | Confirmed shipment date. |
| `trackingNumber` | string | Confirmed carrier tracking number. |

## Native endpoint

Through the native Amazon Seller API, this operation is `POST orders/v0/orders/:orderId/shipmentConfirmation` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/confirm-shipment.md) for the provider-specific parameters and requirements.

