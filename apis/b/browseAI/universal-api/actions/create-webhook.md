# Browse AI: Create Webhook

Creates a webhook in Browse AI.

```
POST https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browse AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "robotId": "c3689adb-50aa-44af-b265-a7e0d4e5846e",
  "hookUrl": "https://example.com/v2/webhooks/callback/events",
  "eventType": "taskFinished"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "robotId": "c3689adb-50aa-44af-b265-a7e0d4e5846e",
    "hookUrl": "https://example.com/v2/webhooks/callback/events",
    "eventType": "taskFinished"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `robotId` | string | yes | Unique robot ID You can find a robot's ID by opening it on the dashboard and copying its ID in the browser address bar. Example: `c3689adb-50aa-44af-b265-a7e0d4e5846e`. |
| `hookUrl` | string | yes | Webhook URL Example: `https://example.com/v2/webhooks/callback/events`. |
| `eventType` | list | yes | One of: `tableExportFinishedSuccessfully`, `taskCapturedDataChanged`, `taskFinished`, `taskFinishedSuccessfully`, `taskFinishedWithError`. Example: `taskFinished`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "id": "string",
      "url": "https://example.com",
      "webhookEvent": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number | Monitor creation date and time in the form of a Unix timestamp. |
| `id` | string | Unique webhook ID |
| `url` | string | Webhook URL |
| `webhookEvent` | string |  |

## Native endpoint

Through the native Browse AI API, this operation is `POST /robots/:robotId/webhooks` (base URL `https://api.browse.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

