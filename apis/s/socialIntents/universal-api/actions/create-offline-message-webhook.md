# Social Intents: Create Offline Message Webhook

Creates an offline message webhook in Social Intents.

```
POST https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/create-offline-message-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Social Intents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/create-offline-message-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "targetUrl": "https://example.com/webhooks/social-intents"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socialIntents/latest/actions/create-offline-message-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "targetUrl": "https://example.com/webhooks/social-intents"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | The Social Intents widget ID that will own the webhook. |
| `targetUrl` | string | yes | The HTTPS endpoint Social Intents should POST webhook events to. Example: `https://example.com/webhooks/social-intents`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Social Intents API, this operation is `POST /apps/:appId/webhook` (base URL `https://www.socialintents.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-offline-message-webhook.md) for the provider-specific parameters and requirements.

