# Svix: Get Poller Token

Retrieves the current Svix poller token.

```
GET https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-poller-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-poller-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-poller-token?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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

Through the native Svix API, this operation is `GET /api/v1/auth/stream/{stream_id}/sink/{sink_id}/poller/token` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-poller-token.md) for the provider-specific parameters and requirements.

