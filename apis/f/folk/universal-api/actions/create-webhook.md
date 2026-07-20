# folk: Create Webhook

Creates a new webhook in folk.

```
POST https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a folk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "targetUrl": "https://example.com",
  "eventType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "targetUrl": "https://example.com",
    "eventType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | A friendly name for the webhook. |
| `targetUrl` | string | yes | The public HTTP or HTTPS URL that receives webhook deliveries. |
| `eventType` | string | yes | The first subscribed webhook event type. |
| `groupId` | string | no | Optionally limit the first subscribed event to a specific Folk group ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "signingSecret": "string",
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
| `signingSecret` | string |  |
| `status` | string |  |
| `subscribedEvents` | array<object> |  |
| `targetUrl` | string |  |

## Native endpoint

Through the native folk API, this operation is `POST /v1/webhooks` (base URL `https://api.folk.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

