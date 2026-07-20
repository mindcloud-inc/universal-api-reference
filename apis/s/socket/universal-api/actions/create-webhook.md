# Socket: Create Webhook

Creates a new webhook in Socket.

```
POST https://connect.mindcloud.co/v1/universal/socket/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/socket/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socket/latest/actions/create-webhook', {
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
      "description": "string",
      "events": [
        "string"
      ],
      "filters": {
        "repositoryIds": [
          "string"
        ]
      },
      "headers": {},
      "id": "string",
      "name": "Ava Chen",
      "secret": "string",
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | The creation date of the webhook |
| `description` | string | The description of the webhook |
| `events` | array<string> |  |
| `filters` | object |  |
| `filters.repositoryIds` | array<string> |  |
| `headers` | object | Custom headers to include in webhook requests |
| `id` | string | The ID of the webhook |
| `name` | string | The name of the webhook |
| `secret` | string | The signing key used to sign webhook payloads |
| `updatedAt` | string | The last update date of the webhook |
| `url` | string | The URL where webhook events will be sent |

## Native endpoint

Through the native Socket API, this operation is `POST /orgs/:org_slug/webhooks` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

