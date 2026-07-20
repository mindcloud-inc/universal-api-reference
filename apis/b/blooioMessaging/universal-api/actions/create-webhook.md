# Blooio Messaging: Create Webhook

Creates a new webhook in Blooio Messaging.

```
POST https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blooio Messaging `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `events` | string | no | Webhook events to subscribe to. |
| `webhookUrl` | string | yes | Webhook callback URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiKeyName": "Ava Chen",
      "createdAt": 1,
      "deprecatedAt": 1,
      "failureCount": 1,
      "isActive": true,
      "lastTriggered": 1,
      "scope": "string",
      "signingSecret": "string",
      "validUntil": 1,
      "webhookId": "string",
      "webhookType": "string",
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKeyName` | string |  |
| `createdAt` | number |  |
| `deprecatedAt` | number |  |
| `failureCount` | number |  |
| `isActive` | boolean |  |
| `lastTriggered` | number |  |
| `scope` | string |  |
| `signingSecret` | string |  |
| `validUntil` | number |  |
| `webhookId` | string |  |
| `webhookType` | string |  |
| `webhookUrl` | string |  |

## Native endpoint

Through the native Blooio Messaging API, this operation is `POST /webhooks` (base URL `https://backend.blooio.com/v2/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

