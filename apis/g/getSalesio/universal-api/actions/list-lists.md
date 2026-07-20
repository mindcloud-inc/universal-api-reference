# GetSales.io: List Lists



```
GET https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/list-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetSales.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/list-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/list-lists?${params}`, {
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
      "name": "Ava Chen",
      "team_id": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `team_id` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native GetSales.io API, this operation is `GET /leads/api/lists` (base URL `https://amazing.getsales.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-lists.md) for the provider-specific parameters and requirements.

