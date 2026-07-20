# OPN: Global Search

Finds records across OPN resources by search query.

```
GET https://connect.mindcloud.co/v1/universal/oPN/latest/actions/global-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/global-search?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/global-search?${params}`, {
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
      "aggregate_level": 1,
      "data": [
        {}
      ],
      "filters": {},
      "location": "string",
      "object": "string",
      "order": "string",
      "page": 1,
      "per_page": 1,
      "query": "string",
      "scope": "string",
      "total": 1,
      "total_pages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aggregate_level` | number |  |
| `data` | array<object> |  |
| `filters` | object |  |
| `location` | string |  |
| `object` | string |  |
| `order` | string |  |
| `page` | number |  |
| `per_page` | number |  |
| `query` | string |  |
| `scope` | string |  |
| `total` | number |  |
| `total_pages` | number |  |

## Native endpoint

Through the native OPN API, this operation is `GET /search` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/global-search.md) for the provider-specific parameters and requirements.

