# Level: List Groups

Retrieves a list of groups from Level.

```
GET https://connect.mindcloud.co/v1/universal/level/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Level `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/level/latest/actions/list-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/level/latest/actions/list-groups?${params}`, {
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
      "data": [
        {
          "childIds": [
            "string"
          ],
          "descendentDeviceCount": 1,
          "deviceCount": 1,
          "id": "string",
          "name": "Ava Chen",
          "parentId": "string"
        }
      ],
      "hasMore": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].childIds` | array<string> |  |
| `data[].descendentDeviceCount` | number |  |
| `data[].deviceCount` | number |  |
| `data[].id` | string |  |
| `data[].name` | string |  |
| `data[].parentId` | string |  |
| `hasMore` | boolean |  |

## Native endpoint

Through the native Level API, this operation is `GET /groups` (base URL `https://api.level.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

