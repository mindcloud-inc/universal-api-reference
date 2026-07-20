# Launch Library 2: List Astronauts



```
GET https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-astronauts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch Library 2 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-astronauts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-astronauts?${params}`, {
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
      "age": 1,
      "agency": {
        "name": "Ava Chen"
      },
      "date_of_birth": "2026-05-07T12:00:00.000Z",
      "flights_count": 1,
      "id": 1,
      "in_space": true,
      "name": "Ava Chen",
      "nationality": [
        {}
      ],
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
| `age` | number |  |
| `agency.name` | string |  |
| `date_of_birth` | date |  |
| `flights_count` | number |  |
| `id` | number |  |
| `in_space` | boolean |  |
| `name` | string |  |
| `nationality` | array<object> |  |
| `status.name` | string |  |
| `type.name` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Launch Library 2 API, this operation is `GET astronauts/` (base URL `https://ll.thespacedevs.com/2.3.0/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-astronauts.md) for the provider-specific parameters and requirements.

