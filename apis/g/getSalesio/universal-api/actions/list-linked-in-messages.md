# GetSales.io: List LinkedIn Messages



```
GET https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/list-linked-in-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetSales.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/list-linked-in-messages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/list-linked-in-messages?${params}`, {
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
        {}
      ],
      "has_more": true,
      "limit": 1,
      "offset": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `has_more` | boolean |  |
| `limit` | number |  |
| `offset` | number |  |
| `total` | number |  |

## Native endpoint

Through the native GetSales.io API, this operation is `GET /flows/api/linkedin-messages` (base URL `https://amazing.getsales.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-linked-in-messages.md) for the provider-specific parameters and requirements.

