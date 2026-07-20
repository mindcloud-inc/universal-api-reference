# Rachio Smart Hose Timer: Create Notification Webhook

Creates a notification webhook for a Rachio device.

```
POST https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/create-notification-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rachio Smart Hose Timer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/create-notification-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "device.id": "string",
  "url": "https://example.com",
  "eventTypes[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/create-notification-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "device.id": "string",
    "url": "https://example.com",
    "eventTypes[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `device.id` | string | yes | Controller device UUID for the webhook target. |
| `url` | string | yes | Webhook destination URL. |
| `externalId` | string | no | Opaque external identifier returned in webhook deliveries. |
| `eventTypes[]` | array<object> | yes | Array of notification webhook event type objects; each item should include an event type id from List Notification Webhook Event Types. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rachio Smart Hose Timer API returns.

## Native endpoint

Through the native Rachio Smart Hose Timer API, this operation is `POST /public/notification/webhook` (base URL `https://api.rach.io/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-notification-webhook.md) for the provider-specific parameters and requirements.

