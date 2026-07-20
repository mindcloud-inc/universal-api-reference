# Lob: List Addresses



```
GET https://connect.mindcloud.co/v1/universal/lob/latest/actions/list-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lob `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lob/latest/actions/list-addresses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lob/latest/actions/list-addresses?${params}`, {
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
      "count": 1,
      "data": [
        {}
      ],
      "next_url": "https://example.com",
      "object": "string",
      "previous_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data` | array<object> |  |
| `next_url` | string |  |
| `object` | string |  |
| `previous_url` | string |  |

## Native endpoint

Through the native Lob API, this operation is `GET /addresses` (base URL `https://api.lob.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-addresses.md) for the provider-specific parameters and requirements.

