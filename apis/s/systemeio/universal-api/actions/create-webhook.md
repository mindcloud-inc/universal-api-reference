# Systeme.io: Create Webhook

Creates a new webhook in Systeme.io.

```
POST https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Systeme.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "secret": "string",
  "url": "https://example.com",
  "subscriptions[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "secret": "string",
    "url": "https://example.com",
    "subscriptions[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Webhook name |
| `secret` | string | yes | Webhook secret |
| `url` | string | yes | Webhook destination URL |
| `subscriptions[]` | array<string> | yes | Webhook event subscriptions Accepts multiple values as an array. |
| `active` | boolean | no | Whether the webhook is active |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "id": "string",
      "name": "Ava Chen",
      "subscriptions": [
        {}
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Webhook activation status. |
| `id` | string | Webhook ID. |
| `name` | string | Webhook name. |
| `subscriptions` | array<object> | Webhook event subscriptions. |
| `url` | string | Webhook target URL. |

## Native endpoint

Through the native Systeme.io API, this operation is `POST /api/webhooks` (base URL `https://api.systeme.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

