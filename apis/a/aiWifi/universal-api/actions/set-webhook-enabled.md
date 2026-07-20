# AiWifi: Set webhook enabled

Updates whether a webhook is active in AiWifi.

```
PUT https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/set-webhook-enabled
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AiWifi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/set-webhook-enabled" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookId": 1,
  "enabled": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/set-webhook-enabled', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookId": 1,
    "enabled": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookId` | number | yes |  |
| `enabled` | boolean | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allEvents": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "emailsToNotify": "ava@example.com",
      "enabled": true,
      "events": [
        {}
      ],
      "id": 1,
      "name": "Ava Chen",
      "notificationThreshold": "string",
      "secret": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allEvents` | boolean |  |
| `createdAt` | date |  |
| `emailsToNotify` | string |  |
| `enabled` | boolean |  |
| `events` | array<object> |  |
| `id` | number |  |
| `name` | string |  |
| `notificationThreshold` | string |  |
| `secret` | string |  |
| `url` | string |  |

## Native endpoint

Through the native AiWifi API, this operation is `PATCH /brands/{{brandId}}/enable/webhook/{{webhookId}}` (base URL `https://api.aiwifi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-webhook-enabled.md) for the provider-specific parameters and requirements.

