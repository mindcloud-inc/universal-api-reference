# Launch Library 2: List Pads



```
GET https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-pads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch Library 2 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-pads?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-pads?${params}`, {
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
      "country": {
        "name": "Ava Chen"
      },
      "description": "string",
      "id": 1,
      "latitude": 1,
      "location": {
        "name": "Ava Chen"
      },
      "longitude": 1,
      "name": "Ava Chen",
      "orbital_launch_attempt_count": 1,
      "total_launch_count": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `country.name` | string |  |
| `description` | string |  |
| `id` | number |  |
| `latitude` | number |  |
| `location.name` | string |  |
| `longitude` | number |  |
| `name` | string |  |
| `orbital_launch_attempt_count` | number |  |
| `total_launch_count` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Launch Library 2 API, this operation is `GET pads/` (base URL `https://ll.thespacedevs.com/2.3.0/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pads.md) for the provider-specific parameters and requirements.

