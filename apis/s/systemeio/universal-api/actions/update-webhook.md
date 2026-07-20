# Systeme.io: Update Webhook

Updates an existing webhook in Systeme.io.

```
PUT https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Systeme.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name": "Ava Chen",
  "secret": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "name": "Ava Chen",
    "secret": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Webhook ID |
| `name` | string | yes | Webhook name |
| `secret` | string | yes | Webhook secret |
| `subscriptions[]` | array<string> | no | Webhook subscriptions Accepts multiple values as an array. |
| `active` | boolean | no | Whether webhook is active |

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

Through the native Systeme.io API, this operation is `PATCH /api/webhooks/:id` (base URL `https://api.systeme.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

