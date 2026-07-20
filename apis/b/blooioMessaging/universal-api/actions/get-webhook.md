# Blooio Messaging: Get Webhook

Retrieves a webhook from Blooio Messaging.

```
GET https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blooio Messaging `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/get-webhook?connectionId=$CONNECTION_ID&webhookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blooioMessaging/latest/actions/get-webhook?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookId` | string | yes | Webhook identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "api_key_name": "Ava Chen",
      "created_at": 1,
      "deprecated_at": 1,
      "failure_count": 1,
      "is_active": true,
      "last_triggered": 1,
      "scope": "string",
      "valid_until": 1,
      "webhook_id": "string",
      "webhook_type": "string",
      "webhook_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_key_name` | string |  |
| `created_at` | number |  |
| `deprecated_at` | number |  |
| `failure_count` | number |  |
| `is_active` | boolean |  |
| `last_triggered` | number |  |
| `scope` | string |  |
| `valid_until` | number |  |
| `webhook_id` | string |  |
| `webhook_type` | string |  |
| `webhook_url` | string |  |

## Native endpoint

Through the native Blooio Messaging API, this operation is `GET /webhooks/{webhookId}` (base URL `https://backend.blooio.com/v2/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

