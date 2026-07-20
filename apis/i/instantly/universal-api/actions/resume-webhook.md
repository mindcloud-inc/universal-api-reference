# Instantly: Resume Webhook

Resumes a webhook in Instantly.

```
PUT https://connect.mindcloud.co/v1/universal/instantly/latest/actions/resume-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/resume-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantly/latest/actions/resume-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Webhook UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event_type": "string",
      "id": "string",
      "name": "Ava Chen",
      "status": 1,
      "target_hook_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event_type` | string | Webhook event type. |
| `id` | string | Unique webhook identifier. |
| `name` | string | Webhook name. |
| `status` | number | Webhook status. |
| `target_hook_url` | string | Target webhook URL. |

## Native endpoint

Through the native Instantly API, this operation is `POST /api/v2/webhooks/:id/resume` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resume-webhook.md) for the provider-specific parameters and requirements.

