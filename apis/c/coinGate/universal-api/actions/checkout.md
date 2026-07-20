# CoinGate: Checkout

Creates a checkout session for an existing CoinGate order.

```
POST https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/checkout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/checkout" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "payCurrency": "string",
  "platformId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/checkout', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "payCurrency": "string",
    "platformId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | CoinGate order ID. |
| `payCurrency` | string | yes | Currency to pay with. |
| `platformId` | number | yes | CoinGate platform ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "doNotConvert": true,
      "id": 1,
      "orderableType": "string",
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `doNotConvert` | boolean |  |
| `id` | number |  |
| `orderableType` | string |  |
| `status` | string |  |
| `title` | string |  |

## Native endpoint

Through the native CoinGate API, this operation is `POST /orders/:id/checkout` (base URL `https://api.coingate.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/checkout.md) for the provider-specific parameters and requirements.

