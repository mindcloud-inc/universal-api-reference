# Rachio Smart Hose Timer: Update Notification Webhook

Updates an existing notification webhook in Rachio.

```
PUT https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/update-notification-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rachio Smart Hose Timer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/update-notification-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "device.id": "string",
  "eventTypes[]": [
    {}
  ],
  "id": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/update-notification-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "device.id": "string",
    "eventTypes[]": [{}],
    "id": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `device.id` | string | yes | Device id for the webhook |
| `eventTypes[]` | array<object> | yes | Webhook event type objects |
| `externalId` | string | no | Optional external identifier |
| `id` | string | yes | Webhook id |
| `url` | string | yes | Webhook callback URL |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rachio Smart Hose Timer API returns.

## Native endpoint

Through the native Rachio Smart Hose Timer API, this operation is `PUT /public/notification/webhook` (base URL `https://api.rach.io/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-notification-webhook.md) for the provider-specific parameters and requirements.

