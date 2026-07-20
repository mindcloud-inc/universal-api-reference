# Gelato: Patch Draft Order v3

Converts a draft order into a regular order in Gelato v3.

```
PUT https://connect.mindcloud.co/v1/universal/gelato/latest/actions/patch-draft-order-v3
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gelato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gelato/latest/actions/patch-draft-order-v3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gelato/latest/actions/patch-draft-order-v3', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | string | yes |  |
| `items[]` | array<object> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Gelato API returns.

## Native endpoint

Through the native Gelato API, this operation is `PATCH /v3/orders/{{orderId}}` (base URL `https://order.gelatoapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-draft-order-v3.md) for the provider-specific parameters and requirements.

