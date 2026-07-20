# Rachio Smart Hose Timer: Create Webhook

Creates a new webhook in Rachio.

```
POST https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rachio Smart Hose Timer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceId": {},
  "url": "https://example.com",
  "eventTypes[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceId": {},
    "url": "https://example.com",
    "eventTypes[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceId` | object | yes | Webhook target resource object, for example {"valveId":"uuid"} or {"irrigationControllerId":"uuid"}. |
| `url` | string | yes | Webhook destination URL. |
| `externalId` | string | no | Opaque identifier echoed back in webhook deliveries. |
| `eventTypes[]` | array<string> | yes | Array of webhook event type strings from List Webhook Event Types. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rachio Smart Hose Timer API returns.

## Native endpoint

Through the native Rachio Smart Hose Timer API, this operation is `POST https://cloud-rest.rach.io/webhook/createWebhook` (base URL `https://api.rach.io/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

