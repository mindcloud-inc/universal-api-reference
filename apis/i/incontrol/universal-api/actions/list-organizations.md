# Incontrol: List Organizations

Retrieves a list of organizations from Incontrol.

```
GET https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Incontrol `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/list-organizations?${params}`, {
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
      "page": 1,
      "perPage": 1,
      "response": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of records returned in this page. |
| `page` | number | Current page number. |
| `perPage` | number | Page size used by the API. |
| `response` | array<object> | Organizations returned for the current page. |

## Native endpoint

Through the native Incontrol API, this operation is `GET /api/v1/organization` (base URL `https://portal.incontrol.app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

