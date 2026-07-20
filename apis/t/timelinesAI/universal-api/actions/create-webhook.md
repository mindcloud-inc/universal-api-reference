# TimelinesAI: Create Webhook

Creates a new webhook subscription in TimelinesAI.

```
POST https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimelinesAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventType": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventType": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventType` | string | yes | Webhook event type to subscribe to. |
| `enabled` | boolean | no | Enable or disable the webhook. |
| `url` | string | yes | Destination URL for webhook deliveries. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "enabled": true,
        "errorsCounter": 1,
        "eventType": "string",
        "id": 1,
        "url": "https://example.com"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.enabled` | boolean |  |
| `data.errorsCounter` | number |  |
| `data.eventType` | string |  |
| `data.id` | number |  |
| `data.url` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TimelinesAI API, this operation is `POST /webhooks` (base URL `https://app.timelines.ai/integrations/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

