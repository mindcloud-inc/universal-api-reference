# folk: Update Webhook

Updates an existing webhook in folk.

```
PUT https://connect.mindcloud.co/v1/universal/folk/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a folk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/folk/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/folk/latest/actions/update-webhook', {
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
| `webhookId` | string | yes | The ID of the webhook to update. |
| `name` | string | no | The updated friendly name for the webhook. |
| `targetUrl` | string | no | The updated public URL that receives webhook deliveries. |
| `eventType` | string | no | The updated first subscribed webhook event type. |
| `groupId` | string | no | Optionally update the first subscribed event filter to a specific Folk group ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "redactedSigningSecret": "string",
      "status": "string",
      "subscribedEvents": [
        {}
      ],
      "targetUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `name` | string |  |
| `redactedSigningSecret` | string |  |
| `status` | string |  |
| `subscribedEvents` | array<object> |  |
| `targetUrl` | string |  |

## Native endpoint

Through the native folk API, this operation is `PATCH /v1/webhooks/:webhookId` (base URL `https://api.folk.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

