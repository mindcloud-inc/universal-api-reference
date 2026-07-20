# Request Tracker (RT): List Queues

Retrieves queues from Request Tracker.

```
GET https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/list-queues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Request Tracker (RT) `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/list-queues?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/list-queues?${params}`, {
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
      "id": "string",
      "type": "string",
      "Url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `type` | string |  |
| `Url` | string |  |

## Native endpoint

Through the native Request Tracker (RT) API, this operation is `GET queues/all` (base URL `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-queues.md) for the provider-specific parameters and requirements.

