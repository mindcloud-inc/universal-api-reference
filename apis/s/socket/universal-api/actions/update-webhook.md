# Socket: Update Webhook

Updates an existing webhook in Socket.

```
PUT https://connect.mindcloud.co/v1/universal/socket/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/socket/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socket/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookId` | string | yes |  |

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

Through the native Socket API, this operation is `PUT /orgs/:org_slug/webhooks/:webhook_id` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

