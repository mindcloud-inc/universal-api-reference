# Timely: Create Webhook

Creates a webhook in Timely.

```
POST https://connect.mindcloud.co/v1/universal/timely/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timely/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "webhook.url": "https://example.com",
  "webhook.subscriptions[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timely/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "webhook.url": "https://example.com",
    "webhook.subscriptions[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | Account ID |
| `webhook.url` | string | yes | URL to send webhook payloads to (must be HTTPS) |
| `webhook.subscriptions[]` | array<string> | yes | List of event types to subscribe to |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhook.secretToken` | string | no | Secret token used to sign webhook payloads. The signature will be included in the X-Signature header. |
| `webhook.active` | string | no | Whether the webhook is active. Defaults to true. Default: `true`. |
| `webhook.customHeaders` | string | no | Custom HTTP headers to include in webhook requests |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": 1,
      "active": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_headers": {},
      "id": 1,
      "secret_token": "string",
      "subscriptions": [
        "string"
      ],
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number |  |
| `active` | boolean |  |
| `created_at` | date |  |
| `custom_headers` | object |  |
| `id` | number |  |
| `secret_token` | string |  |
| `subscriptions` | array<string> |  |
| `updated_at` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Timely API, this operation is `POST /1.1/{account_id}/webhooks` (base URL `https://api.timelyapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

