# Shopkit: Update Client

Updates an existing client in Shopkit.

```
PUT https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/update-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/update-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/update-client', {
  method: 'PUT',
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
      "accepts_marketing": true,
      "billing": {},
      "company": "string",
      "created_at": 1,
      "delivery": {},
      "email": "ava@example.com",
      "hash": "string",
      "id": 1,
      "is_banned": true,
      "is_deleted": true,
      "is_registered": true,
      "last_seen_at": 1,
      "name": "Ava Chen",
      "type": "string",
      "wholesale": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accepts_marketing` | boolean |  |
| `billing` | object |  |
| `company` | string |  |
| `created_at` | number |  |
| `delivery` | object |  |
| `email` | string |  |
| `hash` | string |  |
| `id` | number |  |
| `is_banned` | boolean |  |
| `is_deleted` | boolean |  |
| `is_registered` | boolean |  |
| `last_seen_at` | number |  |
| `name` | string |  |
| `type` | string |  |
| `wholesale` | boolean |  |

## Native endpoint

Through the native Shopkit API, this operation is `PUT /client/:id` (base URL `https://api.shopk.it/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client.md) for the provider-specific parameters and requirements.

