# Engage: List Lists

Retrieves user lists from Engage with pagination.

```
GET https://connect.mindcloud.co/v1/universal/engage/latest/actions/list-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Engage `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/engage/latest/actions/list-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/engage/latest/actions/list-lists?${params}`, {
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
      "broadcastCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "doubleOptin": true,
      "id": "string",
      "redirectUrl": "https://example.com",
      "subscriberCount": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `broadcastCount` | number |  |
| `createdAt` | date |  |
| `description` | string |  |
| `doubleOptin` | boolean |  |
| `id` | string |  |
| `redirectUrl` | string |  |
| `subscriberCount` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Engage API, this operation is `GET /lists` (base URL `https://api.engage.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-lists.md) for the provider-specific parameters and requirements.

