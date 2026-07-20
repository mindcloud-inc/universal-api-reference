# Launch Library 2: List Space Stations



```
GET https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-space-stations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch Library 2 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-space-stations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-space-stations?${params}`, {
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
      "deorbited": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "founded": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "orbit": "string",
      "status": {
        "name": "Ava Chen"
      },
      "type": {
        "name": "Ava Chen"
      },
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deorbited` | date |  |
| `description` | string |  |
| `founded` | date |  |
| `id` | number |  |
| `name` | string |  |
| `orbit` | string |  |
| `status.name` | string |  |
| `type.name` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Launch Library 2 API, this operation is `GET space_stations/` (base URL `https://ll.thespacedevs.com/2.3.0/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-space-stations.md) for the provider-specific parameters and requirements.

