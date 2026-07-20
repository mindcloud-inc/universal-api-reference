# Launch Library 2: List Spacecraft



```
GET https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-spacecraft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch Library 2 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-spacecraft?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-spacecraft?${params}`, {
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
      "flights_count": 1,
      "id": 1,
      "in_space": true,
      "mission_ends_count": 1,
      "name": "Ava Chen",
      "response_mode": "string",
      "serial_number": "string",
      "spacecraft_config": {
        "name": "Ava Chen"
      },
      "status": {
        "name": "Ava Chen"
      },
      "time_docked": "string",
      "time_in_space": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `flights_count` | number |  |
| `id` | number |  |
| `in_space` | boolean |  |
| `mission_ends_count` | number |  |
| `name` | string |  |
| `response_mode` | string |  |
| `serial_number` | string |  |
| `spacecraft_config.name` | string |  |
| `status.name` | string |  |
| `time_docked` | string |  |
| `time_in_space` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Launch Library 2 API, this operation is `GET spacecraft/` (base URL `https://ll.thespacedevs.com/2.3.0/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-spacecraft.md) for the provider-specific parameters and requirements.

