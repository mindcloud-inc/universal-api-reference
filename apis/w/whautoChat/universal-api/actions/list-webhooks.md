# WhautoChat: List Webhooks

Retrieves webhooks from WhautoChat.

```
GET https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhautoChat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/list-webhooks?${params}`, {
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
      "active": true,
      "createdAt": "string",
      "events": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "serverUrl": "https://example.com",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `createdAt` | string |  |
| `events` | array<string> |  |
| `id` | string |  |
| `name` | string |  |
| `serverUrl` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native WhautoChat API, this operation is `GET /v1/webhooks` (base URL `https://api.whauto.chat`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

