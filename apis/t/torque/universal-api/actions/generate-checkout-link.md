# Torque: Generate Checkout Link



```
POST https://connect.mindcloud.co/v1/universal/torque/latest/actions/generate-checkout-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Torque `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/torque/latest/actions/generate-checkout-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cart.items[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/torque/latest/actions/generate-checkout-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cart.items[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cart.items[]` | array<object> | yes | Cart items. Each item needs productId and quantity; variant and metadata are optional. |
| `customerData` | object | no | Optional customer object such as email, name, or metadata. |
| `options` | object | no | Optional checkout settings such as expiresIn or metadata. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "business": {},
      "cartSummary": {},
      "checkoutUrl": "https://example.com",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `business` | object |  |
| `cartSummary` | object |  |
| `checkoutUrl` | string |  |
| `expiresAt` | date |  |
| `success` | boolean |  |

## Native endpoint

Through the native Torque API, this operation is `POST /checkout/generate-link` (base URL `https://app.torque.fi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-checkout-link.md) for the provider-specific parameters and requirements.

