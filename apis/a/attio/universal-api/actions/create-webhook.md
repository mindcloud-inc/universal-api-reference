# Attio: Create Webhook

Creates a webhook in Attio.

```
POST https://connect.mindcloud.co/v1/universal/attio/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Attio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/attio/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetUrl": "https://example.com/webhook",
  "subscriptions[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/attio/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetUrl": "https://example.com/webhook",
    "subscriptions[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targetUrl` | string | yes | The HTTPS URL Attio should send webhook events to. Example: `https://example.com/webhook`. |
| `subscriptions[]` | array<object> | yes | Webhook subscriptions array using Attio's documented event_type and optional filter objects. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": {},
      "secret": "string",
      "status": "string",
      "subscriptions": [
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
| `createdAt` | date | When the webhook was created. |
| `id` | object | Webhook identifier payload containing workspace and webhook ids. |
| `secret` | string | Webhook secret returned at creation time. |
| `status` | string | Webhook status. |
| `subscriptions` | array<object> | Webhook subscription definitions. |
| `targetUrl` | string | Destination URL for webhook deliveries. |

## Native endpoint

Through the native Attio API, this operation is `POST /v2/webhooks` (base URL `https://api.attio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

