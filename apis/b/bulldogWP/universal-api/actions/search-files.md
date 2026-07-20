# Bulldog-WP: Search files

Finds files in Bulldog-WP.

```
GET https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/search-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bulldog-WP `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/search-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/search-files?${params}`, {
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
      "contact": "string",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "format": "string",
      "id": "string",
      "lastAccessAt": "2026-05-07T12:00:00.000Z",
      "lastDeliveryAt": "2026-05-07T12:00:00.000Z",
      "origin": "string",
      "permission": 1,
      "status": 1,
      "url": "https://example.com",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | string |  |
| `deletedAt` | date |  |
| `expiresAt` | date |  |
| `format` | string |  |
| `id` | string |  |
| `lastAccessAt` | date |  |
| `lastDeliveryAt` | date |  |
| `origin` | string |  |
| `permission` | number |  |
| `status` | number |  |
| `url` | string |  |
| `user` | object |  |

## Native endpoint

Through the native Bulldog-WP API, this operation is `GET /files` (base URL `https://api.bulldog-wp.co.il/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-files.md) for the provider-specific parameters and requirements.

