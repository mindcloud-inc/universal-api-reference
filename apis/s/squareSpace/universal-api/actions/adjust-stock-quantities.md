# SquareSpace: Adjust Stock Quantities

Updates stock quantities in Squarespace.

```
PUT https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/adjust-stock-quantities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SquareSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/adjust-stock-quantities" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idempotencyKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/adjust-stock-quantities', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "idempotencyKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `decrementOperations[]` | array<object> | no | Operations to decrement finite stock quantities. |
| `decrementOperations[].quantity` | number | no | Quantity to decrement. |
| `decrementOperations[].variantId` | list<string> | no | Variant ID to decrement. |
| `idempotencyKey` | string | yes | Unique idempotency key for safe stock-adjustment retries. |
| `incrementOperations[]` | array<object> | no | Operations to increment finite stock quantities. |
| `incrementOperations[].quantity` | number | no | Quantity to increment. |
| `incrementOperations[].variantId` | list<string> | no | Variant ID to increment. |
| `setFiniteOperations[]` | array<object> | no | Operations to set finite stock quantities. |
| `setFiniteOperations[].quantity` | number | no | Finite quantity to set. |
| `setFiniteOperations[].variantId` | list<string> | no | Variant ID for finite stock set operation. |
| `setUnlimitedOperations[]` | array<string> | no | Variant IDs to set as unlimited stock. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SquareSpace API returns.

## Native endpoint

Through the native SquareSpace API, this operation is `POST /1.0/commerce/inventory/adjustments` (base URL `https://api.squarespace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/adjust-stock-quantities.md) for the provider-specific parameters and requirements.

