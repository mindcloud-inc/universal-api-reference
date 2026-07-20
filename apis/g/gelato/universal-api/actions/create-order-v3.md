# Gelato: Create Order v3

Creates an order in Gelato v3.

```
POST https://connect.mindcloud.co/v1/universal/gelato/latest/actions/create-order-v3
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gelato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gelato/latest/actions/create-order-v3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderReferenceId": "string",
  "customerReferenceId": "string",
  "currency": "string",
  "items[]": [
    {}
  ],
  "shippingAddress": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gelato/latest/actions/create-order-v3', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderReferenceId": "string",
    "customerReferenceId": "string",
    "currency": "string",
    "items[]": [{}],
    "shippingAddress": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderReferenceId` | string | yes |  |
| `customerReferenceId` | string | yes |  |
| `currency` | string | yes |  |
| `items[]` | array<object> | yes |  |
| `shippingAddress` | object | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Gelato API returns.

## Native endpoint

Through the native Gelato API, this operation is `POST /v3/orders` (base URL `https://order.gelatoapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order-v3.md) for the provider-specific parameters and requirements.

