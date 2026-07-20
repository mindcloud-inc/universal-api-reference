# AiWifi: Create webhook

Creates a new webhook configuration in AiWifi.

```
POST https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AiWifi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "url": "https://example.com",
  "allEvents": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "url": "https://example.com",
    "allEvents": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `url` | string | yes |  |
| `allEvents` | boolean | yes | Default: `true`. |
| `eventCodes` | list<string> | no | One of: `guest.connected`, `guest.data`, `guest.interests`, `surveyAnswer.created`. Accepts multiple values as an array. |

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
        "string"
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
| `events` | array |  |
| `id` | number |  |
| `name` | string |  |
| `notificationThreshold` | string |  |
| `secret` | string |  |
| `url` | string |  |

## Native endpoint

Through the native AiWifi API, this operation is `POST /brands/{{brandId}}/webhook-configs` (base URL `https://api.aiwifi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

