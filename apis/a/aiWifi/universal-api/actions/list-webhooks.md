# AiWifi: List webhooks

Retrieves webhook configurations from AiWifi.

```
GET https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AiWifi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/list-webhooks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native AiWifi API, this operation is `GET /brands/{{brandId}}/webhook-configs` (base URL `https://api.aiwifi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

