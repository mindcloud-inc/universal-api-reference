# Launch Library 2: List Agencies



```
GET https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-agencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch Library 2 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-agencies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchLibrary2/latest/actions/list-agencies?${params}`, {
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
      "abbrev": "string",
      "country": [
        {}
      ],
      "description": "string",
      "featured": true,
      "founding_year": 1,
      "id": 1,
      "name": "Ava Chen",
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
| `abbrev` | string |  |
| `country` | array<object> |  |
| `description` | string |  |
| `featured` | boolean |  |
| `founding_year` | number |  |
| `id` | number |  |
| `name` | string |  |
| `type.name` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Launch Library 2 API, this operation is `GET agencies/` (base URL `https://ll.thespacedevs.com/2.3.0/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-agencies.md) for the provider-specific parameters and requirements.

