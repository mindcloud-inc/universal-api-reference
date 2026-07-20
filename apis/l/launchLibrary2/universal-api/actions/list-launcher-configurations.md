# Launch Library 2: List Launcher Configurations



```
GET https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-launcher-configurations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch Library 2 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-launcher-configurations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-launcher-configurations?${params}`, {
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
      "full_name": "Ava Chen",
      "id": 1,
      "manufacturer": {
        "name": "Ava Chen"
      },
      "name": "Ava Chen",
      "response_mode": "string",
      "reusable": true,
      "url": "https://example.com",
      "variant": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `full_name` | string |  |
| `id` | number |  |
| `manufacturer.name` | string |  |
| `name` | string |  |
| `response_mode` | string |  |
| `reusable` | boolean |  |
| `url` | string |  |
| `variant` | string |  |

## Native endpoint

Through the native Launch Library 2 API, this operation is `GET launcher_configurations/` (base URL `https://ll.thespacedevs.com/2.3.0/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-launcher-configurations.md) for the provider-specific parameters and requirements.

