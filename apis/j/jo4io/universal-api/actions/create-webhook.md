# jo4.io: Create Webhook



```
POST https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a jo4.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `events` | string | no |  |
| `name` | string | yes |  |
| `url` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": 1,
      "enabled": true,
      "events": "string",
      "failureCount": 1,
      "id": 1,
      "lastError": "string",
      "lastTriggeredAt": 1,
      "modifiedTime": 1,
      "name": "Ava Chen",
      "secret": "string",
      "slug": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | number |  |
| `enabled` | boolean |  |
| `events` | string |  |
| `failureCount` | number |  |
| `id` | number |  |
| `lastError` | string |  |
| `lastTriggeredAt` | number |  |
| `modifiedTime` | number |  |
| `name` | string |  |
| `secret` | string |  |
| `slug` | string |  |
| `url` | string |  |

## Native endpoint

Through the native jo4.io API, this operation is `POST /protected/webhooks` (base URL `https://jo4-api.jo4.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

