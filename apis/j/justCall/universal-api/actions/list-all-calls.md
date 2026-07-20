# JustCall: List All Calls

Retrieves calls from JustCall.

```
GET https://connect.mindcloud.co/v1/universal/justCall/latest/actions/list-all-calls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JustCall `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/justCall/latest/actions/list-all-calls?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/justCall/latest/actions/list-all-calls?${params}`, {
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
      "currentPage": 1,
      "data": [
        {}
      ],
      "nextPageLink": "https://example.com",
      "perPage": 1,
      "prevPageLink": "https://example.com",
      "status": "string",
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `currentPage` | number |  |
| `data` | array<object> |  |
| `nextPageLink` | string |  |
| `perPage` | number |  |
| `prevPageLink` | string |  |
| `status` | string |  |
| `totalCount` | number |  |

## Native endpoint

Through the native JustCall API, this operation is `GET /v2.1/calls` (base URL `https://api.justcall.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-all-calls.md) for the provider-specific parameters and requirements.

