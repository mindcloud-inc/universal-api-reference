# CoinGate: Create Order

Creates a new order in CoinGate.

```
POST https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "priceAmount": 1,
  "priceCurrency": "string",
  "title": "string",
  "description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "priceAmount": 1,
    "priceCurrency": "string",
    "title": "string",
    "description": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `priceAmount` | number | yes | Order price amount. |
| `priceCurrency` | string | yes | Order price currency. |
| `title` | string | yes | Order title. |
| `description` | string | yes | Order description. |

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

Through the native CoinGate API, this operation is `POST /orders` (base URL `https://api.coingate.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

