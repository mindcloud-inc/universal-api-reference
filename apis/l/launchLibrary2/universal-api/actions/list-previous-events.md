# Launch Library 2: List Previous Events



```
GET https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-previous-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch Library 2 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-previous-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-previous-events?${params}`, {
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
      "date": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "location": "string",
      "name": "Ava Chen",
      "slug": "string",
      "type": {
        "name": "Ava Chen"
      },
      "url": "https://example.com",
      "webcast_live": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date |  |
| `description` | string |  |
| `id` | number |  |
| `location` | string |  |
| `name` | string |  |
| `slug` | string |  |
| `type.name` | string |  |
| `url` | string |  |
| `webcast_live` | boolean |  |

## Native endpoint

Through the native Launch Library 2 API, this operation is `GET events/previous/` (base URL `https://ll.thespacedevs.com/2.3.0/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-previous-events.md) for the provider-specific parameters and requirements.

