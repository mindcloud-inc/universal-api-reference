# OPN: Create Source

Creates a new source in OPN.

```
POST https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-source', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "bank": "string",
      "barcode": "string",
      "charge_status": "string",
      "created_at": "string",
      "currency": "string",
      "email": "ava@example.com",
      "flow": "string",
      "id": "string",
      "livemode": true,
      "location": "string",
      "name": "Ava Chen",
      "object": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `bank` | string |  |
| `barcode` | string |  |
| `charge_status` | string |  |
| `created_at` | string |  |
| `currency` | string |  |
| `email` | string |  |
| `flow` | string |  |
| `id` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `name` | string |  |
| `object` | string |  |
| `type` | string |  |

## Native endpoint

Through the native OPN API, this operation is `POST /sources` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-source.md) for the provider-specific parameters and requirements.

