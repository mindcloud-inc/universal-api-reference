# vPlan: Create Webhook



```
POST https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "api_key_id": "string",
      "can_send": true,
      "created_at": "string",
      "description": "string",
      "developer_client_id": "string",
      "disabled_until": "string",
      "event_types": [
        "string"
      ],
      "fail_streak": "string",
      "fail_streak_started_at": "string",
      "id": "string",
      "last_failed_at": "string",
      "mailed_disabled_at": "string",
      "mailed_warning_at": "string",
      "third_party": true,
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
| `active` | boolean | Whether the webhook is active. |
| `api_key_id` | string | API key identifier. |
| `can_send` | boolean | Whether the webhook can currently send. |
| `created_at` | string | Creation timestamp. |
| `description` | string | Webhook description. |
| `developer_client_id` | string | Developer client identifier. |
| `disabled_until` | string | Disabled until timestamp. |
| `event_types` | array<string> | Subscribed event types. |
| `fail_streak` | string | Consecutive failure count. |
| `fail_streak_started_at` | string | Failure streak start timestamp. |
| `id` | string | Webhook identifier. |
| `last_failed_at` | string | Last failure timestamp. |
| `mailed_disabled_at` | string | Disabled email timestamp. |
| `mailed_warning_at` | string | Warning email timestamp. |
| `third_party` | boolean | Whether this is a third-party webhook. |
| `updated_at` | string | Last update timestamp. |
| `url` | string | Webhook destination URL. |

## Native endpoint

Through the native vPlan API, this operation is `POST /webhook` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

