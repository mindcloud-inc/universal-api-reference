# MailerLite: Create Webhook

Creates a new webhook in MailerLite.

```
POST https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerLite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "events[]": "subscriber.created",
  "url": "https://webhook.site/your-test-endpoint"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "events[]": "subscriber.created",
    "url": "https://webhook.site/your-test-endpoint"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Friendly name for the webhook. Example: `MC Wizard Stage3 Webhook`. |
| `events[]` | array<string> | yes | Webhook events to subscribe to. Example: `subscriber.created`. |
| `url` | string | yes | Destination URL for MailerLite webhook deliveries. Example: `https://webhook.site/your-test-endpoint`. |
| `enabled` | boolean | no | Whether the webhook is enabled immediately after creation. Default: `false`. |
| `batchable` | boolean | no | Whether MailerLite can batch event deliveries for this webhook. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchable": true,
      "createdAt": "string",
      "enabled": true,
      "events": [
        "string"
      ],
      "id": "string",
      "isBlocked": true,
      "lastFiredAt": "string",
      "name": "Ava Chen",
      "responseCode": 1,
      "updatedAt": "string",
      "url": "https://example.com",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchable` | boolean |  |
| `createdAt` | string |  |
| `enabled` | boolean |  |
| `events` | array<string> |  |
| `id` | string |  |
| `isBlocked` | boolean |  |
| `lastFiredAt` | string |  |
| `name` | string |  |
| `responseCode` | number |  |
| `updatedAt` | string |  |
| `url` | string |  |
| `version` | string |  |

## Native endpoint

Through the native MailerLite API, this operation is `POST /webhooks` (base URL `https://connect.mailerlite.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

