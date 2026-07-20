# Superchat: Update Webhook

Updates an existing webhook in Superchat.

```
PUT https://connect.mindcloud.co/v1/universal/superchat/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superchat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/superchat/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhook_id": "string",
  "target_url": "https://example.com",
  "events[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superchat/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhook_id": "string",
    "target_url": "https://example.com",
    "events[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhook_id` | string | yes | The unique identifier of the webhook |
| `target_url` | string | yes | The target URL for the webhook. Must use `https://` |
| `events[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "events": [
        {}
      ],
      "id": "string",
      "status": "string",
      "target_url": "https://example.com",
      "updated_at": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `events` | array<object> |  |
| `id` | string |  |
| `status` | string |  |
| `target_url` | string |  |
| `updated_at` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Superchat API, this operation is `PUT /webhooks/{webhook_id}` (base URL `https://api.superchat.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

