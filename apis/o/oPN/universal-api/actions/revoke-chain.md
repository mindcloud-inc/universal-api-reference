# OPN: Revoke Chain

Revokes an existing chain in OPN.

```
PUT https://connect.mindcloud.co/v1/universal/oPN/latest/actions/revoke-chain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/revoke-chain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oPN/latest/actions/revoke-chain', {
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
      "created_at": "string",
      "email": "ava@example.com",
      "id": "string",
      "key": "string",
      "livemode": true,
      "location": "string",
      "object": "string",
      "revoked": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `email` | string |  |
| `id` | string |  |
| `key` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `object` | string |  |
| `revoked` | boolean |  |

## Native endpoint

Through the native OPN API, this operation is `POST /chains/:id/revoke` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/revoke-chain.md) for the provider-specific parameters and requirements.

