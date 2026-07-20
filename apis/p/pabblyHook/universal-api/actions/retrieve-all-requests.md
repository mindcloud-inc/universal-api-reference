# Pabbly Hook: Retrieve All Requests



```
GET https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/retrieve-all-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Hook `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/retrieve-all-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/retrieve-all-requests?${params}`, {
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
      "currentPage": 1,
      "data": [
        {}
      ],
      "page": 1,
      "total": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number | Current page number when returned as currentPage. |
| `data` | array<object> | Request records returned by Pabbly Hook. |
| `page` | number | Current page number. |
| `total` | number | Total request records. |
| `totalPages` | number | Total number of pages. |

## Native endpoint

Through the native Pabbly Hook API, this operation is `GET /api/v1/requests` (base URL `https://hook.pabbly.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/retrieve-all-requests.md) for the provider-specific parameters and requirements.

