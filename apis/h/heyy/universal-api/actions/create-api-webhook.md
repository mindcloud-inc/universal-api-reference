# Heyy: Create API Webhook

Creates a new API webhook in Heyy.

```
POST https://connect.mindcloud.co/v1/universal/heyy/latest/actions/create-api-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heyy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/heyy/latest/actions/create-api-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tenantId": "string",
  "type": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heyy/latest/actions/create-api-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tenantId": "string",
    "type": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | no | The channel ID for the webhook. |
| `tenantId` | string | yes | The Heyy tenant ID. |
| `type` | string | yes | The webhook event type. |
| `url` | string | yes | The webhook destination URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isActive": true,
      "tenantId": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelId` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `tenantId` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Heyy API, this operation is `POST /api_webhooks` (base URL `https://api.heyy.io/api/v2.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-api-webhook.md) for the provider-specific parameters and requirements.

