# Wooxy: Create Webhook

Creates a new webhook in Wooxy.

```
POST https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "stage3-webhook",
  "url": "https://example.com/webhook",
  "events[]": "delivered"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "stage3-webhook",
    "url": "https://example.com/webhook",
    "events[]": "delivered"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Webhook title. Example: `stage3-webhook`. |
| `url` | string | yes | Callback URL that receives webhook events. Example: `https://example.com/webhook`. |
| `domainId` | string | no | Verified Wooxy domain ID. Example: `yourDomainId`. |
| `domain` | string | no | Verified Wooxy domain name. Example: `mindcloud.co`. |
| `events[]` | array<string> | yes | Webhook event names. Default: `["delivered"]`. Example: `delivered`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Wooxy API returns.

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/webhook/create` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

