# Launch Library 2: List Programs



```
GET https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-programs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch Library 2 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-programs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-programs?${params}`, {
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
      "description": "string",
      "end_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "info_url": "https://example.com",
      "name": "Ava Chen",
      "response_mode": "string",
      "start_date": "2026-05-07T12:00:00.000Z",
      "type": {
        "name": "Ava Chen"
      },
      "url": "https://example.com",
      "wiki_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `end_date` | date |  |
| `id` | number |  |
| `info_url` | string |  |
| `name` | string |  |
| `response_mode` | string |  |
| `start_date` | date |  |
| `type.name` | string |  |
| `url` | string |  |
| `wiki_url` | string |  |

## Native endpoint

Through the native Launch Library 2 API, this operation is `GET programs/` (base URL `https://ll.thespacedevs.com/2.3.0/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-programs.md) for the provider-specific parameters and requirements.

