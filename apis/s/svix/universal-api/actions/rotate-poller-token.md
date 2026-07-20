# Svix: Rotate Poller Token

Rotates the current Svix poller token.

```
POST https://connect.mindcloud.co/v1/universal/svix/latest/actions/rotate-poller-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/svix/latest/actions/rotate-poller-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/svix/latest/actions/rotate-poller-token', {
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
      "createdAt": "string",
      "expiresAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "scopes": [
        "string"
      ],
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `expiresAt` | string |  |
| `id` | string |  |
| `name` | string |  |
| `scopes` | array<string> |  |
| `token` | string |  |

## Native endpoint

Through the native Svix API, this operation is `POST /api/v1/auth/stream/{stream_id}/sink/{sink_id}/poller/token/rotate` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rotate-poller-token.md) for the provider-specific parameters and requirements.

