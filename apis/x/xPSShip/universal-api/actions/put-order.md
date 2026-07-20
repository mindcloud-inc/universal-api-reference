# XPS Ship: Put Order

Creates or updates an order in XPS Ship.

```
PUT https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/put-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XPS Ship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/put-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "integrationId": "string",
  "orderId": "string",
  "bodyOrderId": "string",
  "orderDate": "string",
  "orderNumber": "string",
  "fulfillmentStatus": "string",
  "shippingService": "string",
  "shippingTotal": "string",
  "weightUnit": "string",
  "dimUnit": "string",
  "dueByDate": "string",
  "orderGroup": "string",
  "sender": {},
  "receiver": {},
  "items": {},
  "packages": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/put-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "integrationId": "string",
    "orderId": "string",
    "bodyOrderId": "string",
    "orderDate": "string",
    "orderNumber": "string",
    "fulfillmentStatus": "string",
    "shippingService": "string",
    "shippingTotal": "string",
    "weightUnit": "string",
    "dimUnit": "string",
    "dueByDate": "string",
    "orderGroup": "string",
    "sender": {},
    "receiver": {},
    "items": {},
    "packages": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `integrationId` | string | yes | XPS Ship REST API integration ID. |
| `orderId` | string | yes | Unique order ID, matching the orderId in the request body. |
| `bodyOrderId` | string | yes | Required order ID in the JSON body; must match the URL order ID. |
| `orderDate` | string | yes | Date the order was placed. |
| `orderNumber` | string | yes | Invoice number of the order, or null. |
| `fulfillmentStatus` | string | yes | One of pending, fulfilled, or partial. |
| `shippingService` | string | yes | Name of shipping service associated with order, or null. |
| `shippingTotal` | string | yes | Amount the customer paid for shipping, or null. |
| `weightUnit` | string | yes | Weight unit, lb or kg, or null. |
| `dimUnit` | string | yes | Dimension unit, in or cm, or null. |
| `dueByDate` | string | yes | Date by which the order must be fulfilled, or null. |
| `orderGroup` | string | yes | Group for multi-user shipping, or null. |
| `sender` | object | yes | Required sender address object. |
| `receiver` | object | yes | Required receiver address object. |
| `items` | list<object> | yes | Order item array, or null. Accepts multiple values as an array. |
| `packages` | list<object> | yes | Package array, or null. Accepts multiple values as an array. |
| `shipperReference` | string | no | Optional reference text to show on the shipping label. |
| `shipperReference2` | string | no | Optional second reference field for the label when supported by the carrier. |
| `contentDescription` | string | no | Optional content description of the shipment. |
| `returnTo` | object | no | Optional return-to address object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean | True when the order was created or updated. |

## Native endpoint

Through the native XPS Ship API, this operation is `PUT /restapi/v1/customers/:customerId/integrations/:integrationId/orders/:orderId` (base URL `https://xpsshipper.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/put-order.md) for the provider-specific parameters and requirements.

