# Universe: Get Order Item

Retrieves a specific order item from Universe.

```
GET https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-order-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-order-item?connectionId=$CONNECTION_ID&query=query%20GetOrderItem(%24orderItemId%3A%20ID!)%20%7B%0A%20%20orderItem(id%3A%20%24orderItemId)%20%7B%0A%20%20%20%20id%0A%20%20%20%20name%0A%20%20%20%20state%0A%20%20%20%20checkInState%0A%20%20%20%20qrCode%0A%20%20%20%20firstName%0A%20%20%20%20lastName%0A%20%20%20%20order%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%20%20ref%0A%20%20%20%20%20%20state%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query GetOrderItem($orderItemId: ID!) {\n  orderItem(id: $orderItemId) {\n    id\n    name\n    state\n    checkInState\n    qrCode\n    firstName\n    lastName\n    order {\n      id\n      ref\n      state\n    }\n  }\n}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-order-item?${params}`, {
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
| `query` | string | yes | Universe GraphQL query or mutation document to execute. The default is an order item detail example for this action. Default: `query GetOrderItem($orderItemId: ID!) {\n  orderItem(id: $orderItemId) {\n    id\n    name\n    state\n    checkInState\n    qrCode\n    firstName\n    lastName\n    order {\n      id\n      ref\n      state\n    }\n  }\n}`. |
| `variables` | object | no | Optional GraphQL variables as a JSON object string for the default order item query. Default: `{"orderItemId":"ORDER_ITEM_ID"}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Universe API returns.

## Native endpoint

Through the native Universe API, this operation is `POST /graphql` (base URL `https://www.universe.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-item.md) for the provider-specific parameters and requirements.

