# TimelinesAI: Get Webhook

Retrieves details for a TimelinesAI webhook subscription.

```
GET https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimelinesAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/get-webhook?connectionId=$CONNECTION_ID&webhookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/get-webhook?${params}`, {
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
| `webhookId` | string | yes | ID of the webhook in TimelinesAI. |

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

Through the native TimelinesAI API, this operation is `GET /webhooks/{webhook_id}` (base URL `https://app.timelines.ai/integrations/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

