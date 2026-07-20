# Universe: Get Order

Retrieves a specific order from Universe.

```
GET https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-order?connectionId=$CONNECTION_ID&query=query%20GetOrder(%24orderId%3A%20ID!)%20%7B%0A%20%20order(id%3A%20%24orderId)%20%7B%0A%20%20%20%20id%0A%20%20%20%20ref%0A%20%20%20%20state%0A%20%20%20%20createdAt%0A%20%20%20%20updatedAt%0A%20%20%20%20accessKeys%0A%20%20%20%20validOrderItemsCount%0A%20%20%20%20event%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%20%20title%0A%20%20%20%20%7D%0A%20%20%20%20orderItems%20%7B%0A%20%20%20%20%20%20nodes%20%7B%0A%20%20%20%20%20%20%20%20id%0A%20%20%20%20%20%20%20%20name%0A%20%20%20%20%20%20%20%20state%0A%20%20%20%20%20%20%20%20checkInState%0A%20%20%20%20%20%20%20%20qrCode%0A%20%20%20%20%20%20%7D%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query GetOrder($orderId: ID!) {\n  order(id: $orderId) {\n    id\n    ref\n    state\n    createdAt\n    updatedAt\n    accessKeys\n    validOrderItemsCount\n    event {\n      id\n      title\n    }\n    orderItems {\n      nodes {\n        id\n        name\n        state\n        checkInState\n        qrCode\n      }\n    }\n  }\n}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-order?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | Universe GraphQL query or mutation document to execute. The default is an order detail example for this action. Default: `query GetOrder($orderId: ID!) {\n  order(id: $orderId) {\n    id\n    ref\n    state\n    createdAt\n    updatedAt\n    accessKeys\n    validOrderItemsCount\n    event {\n      id\n      title\n    }\n    orderItems {\n      nodes {\n        id\n        name\n        state\n        checkInState\n        qrCode\n      }\n    }\n  }\n}`. |
| `variables` | object | no | Optional GraphQL variables as a JSON object string for the default order query. Default: `{"orderId":"ORDER_ID"}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Universe API returns.

## Native endpoint

Through the native Universe API, this operation is `POST /graphql` (base URL `https://www.universe.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

