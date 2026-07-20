# eCFR: Get Hierarchy Search Counts

Retrieves search result counts by hierarchy from eCFR.

```
GET https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/get-hierarchy-search-counts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eCFR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/get-hierarchy-search-counts?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/get-hierarchy-search-counts?${params}`, {
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
| `query` | string | yes | Search query text for hierarchy counts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "children": [
        {}
      ],
      "count": {},
      "max_score": 1,
      "shown_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `children` | array<object> | Hierarchical count buckets. |
| `count` | object | Total hierarchy search count information. |
| `max_score` | number | Maximum search score. |
| `shown_count` | number | Number of shown hierarchy records. |

## Native endpoint

Through the native eCFR API, this operation is `GET /api/search/v1/counts/hierarchy` (base URL `https://www.ecfr.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hierarchy-search-counts.md) for the provider-specific parameters and requirements.

