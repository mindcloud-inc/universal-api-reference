# Starshipit: Create Tracking Only Order



```
POST https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/create-tracking-only-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/create-tracking-only-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/create-tracking-only-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orders[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orders": {
        "398667087": "string",
        "398667099": "string",
        "398667108": "string",
        "398667112": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orders` | object |  |
| `orders.398667087` | string |  |
| `orders.398667099` | string |  |
| `orders.398667108` | string |  |
| `orders.398667112` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Starshipit API, this operation is `POST /orders/shipped` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tracking-only-order.md) for the provider-specific parameters and requirements.

