# OPN: Create Webhook Secret

Creates a new webhook Secret in OPN.

```
POST https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-webhook-secret
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-webhook-secret" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-webhook-secret', {
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
      "created_at": "string",
      "expires_at": "string",
      "expiring": true,
      "id": "string",
      "key": "string",
      "livemode": true,
      "object": "string",
      "revoked_at": "string",
      "usable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `expires_at` | string |  |
| `expiring` | boolean |  |
| `id` | string |  |
| `key` | string |  |
| `livemode` | boolean |  |
| `object` | string |  |
| `revoked_at` | string |  |
| `usable` | boolean |  |

## Native endpoint

Through the native OPN API, this operation is `POST /webhooks/secrets` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-secret.md) for the provider-specific parameters and requirements.

