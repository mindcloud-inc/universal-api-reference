# AiWifi: List webhook logs

Retrieves webhook delivery logs from AiWifi.

```
GET https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/list-webhook-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AiWifi `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/list-webhook-logs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aiWifi/latest/actions/list-webhook-logs?${params}`, {
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
      "code": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "eventId": "string",
      "eventType": "string",
      "id": 1,
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `createdAt` | date |  |
| `eventId` | string |  |
| `eventType` | string |  |
| `id` | number |  |
| `status` | string |  |
| `url` | string |  |

## Native endpoint

Through the native AiWifi API, this operation is `GET /brands/{{brandId}}/webhook-logs` (base URL `https://api.aiwifi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-webhook-logs.md) for the provider-specific parameters and requirements.

