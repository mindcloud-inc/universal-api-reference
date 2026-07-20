# Universe: Check Out Order Item

Checks out a specific Universe order item.

```
PUT https://connect.mindcloud.co/v1/universal/universe/latest/actions/check-out-order-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/universe/latest/actions/check-out-order-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "mutation CheckOutOrderItem($input: OrderItemCheckOutInput!) {\n  orderItemCheckOut(input: $input) {\n    errors\n    orderItem {\n      id\n      checkInState\n      state\n      qrCode\n    }\n  }\n}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/universe/latest/actions/check-out-order-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "mutation CheckOutOrderItem($input: OrderItemCheckOutInput!) {\n  orderItemCheckOut(input: $input) {\n    errors\n    orderItem {\n      id\n      checkInState\n      state\n      qrCode\n    }\n  }\n}"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | Universe GraphQL query or mutation document to execute. The default is an order-item check-out mutation for this action. Default: `mutation CheckOutOrderItem($input: OrderItemCheckOutInput!) {\n  orderItemCheckOut(input: $input) {\n    errors\n    orderItem {\n      id\n      checkInState\n      state\n      qrCode\n    }\n  }\n}`. |
| `variables` | object | no | Optional GraphQL variables as a JSON object string for the default check-out mutation. Default: `{"input":{"id":"ORDER_ITEM_ID"}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checkInState": "string",
      "errors": [
        "string"
      ],
      "id": "string",
      "orderItem": {},
      "orderItemCheckOut": {},
      "qrCode": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkInState` | string | Check-in state after checkout. |
| `errors` | array<string> | Mutation errors if present. |
| `id` | string | Order item id. |
| `orderItem` | object | Updated order item ticket. |
| `orderItemCheckOut` | object | Check-out mutation result. |
| `qrCode` | string | Order item QR code. |
| `state` | string | Order item state. |

## Native endpoint

Through the native Universe API, this operation is `POST /graphql` (base URL `https://www.universe.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-out-order-item.md) for the provider-specific parameters and requirements.

