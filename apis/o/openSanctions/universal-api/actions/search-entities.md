# OpenSanctions: Search Entities



```
GET https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/search-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSanctions `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/search-entities?connectionId=$CONNECTION_ID&limit=25&offset=0&dataset=default" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "dataset": "default"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/search-entities?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataset` | string | yes | Data source or collection name to scope the search to. Default: `default`. |
| `q` | string | no | Query text to search for. Default: `Vladimir Putin`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `schema` | string | no | Entity schema type to search within. The API default is Thing. Default: `Thing`. |
| `simple` | boolean | no | Use simple syntax for user-facing query boxes. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "facets": {},
      "limit": 1,
      "offset": 1,
      "results": [
        {}
      ],
      "total": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `facets` | object | Facet buckets returned by the search endpoint. |
| `limit` | number | Number of results requested. |
| `offset` | number | Offset of the result set. |
| `results` | array<object> | Matching entity results. |
| `total` | object | Total result count metadata. |

## Native endpoint

Through the native OpenSanctions API, this operation is `GET /search/:dataset` (base URL `https://api.opensanctions.org`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-entities.md) for the provider-specific parameters and requirements.

