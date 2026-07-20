# jo4.io: List My Webhooks



```
GET https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/get-my-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a jo4.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/get-my-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/get-my-webhooks?${params}`, {
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

Through the native jo4.io API, this operation is `GET /protected/webhooks` (base URL `https://jo4-api.jo4.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-webhooks.md) for the provider-specific parameters and requirements.

