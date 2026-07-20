# Cryptlex: Create Webhook

Creates a webhook in Cryptlex.

```
POST https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptlex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "enabled": true,
  "events[]": [
    "string"
  ],
  "name": "Ava Chen",
  "token": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "enabled": true,
    "events[]": ["string"],
    "name": "Ava Chen",
    "token": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `enabled` | boolean | yes | Whether the webhook is enabled. |
| `events[]` | array<string> | yes | Events to subscribe the webhook to. Accepts multiple values as an array. |
| `name` | string | yes | Webhook name. |
| `token` | string | yes | Shared secret token for webhook verification. |
| `url` | string | yes | Destination URL for the webhook. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
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
| `createdAt` | date |  |
| `enabled` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Cryptlex API, this operation is `POST /v3/webhooks` (base URL `https://api.cryptlex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

