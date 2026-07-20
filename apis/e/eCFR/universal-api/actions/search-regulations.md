# eCFR: Search Regulations

Searches regulations in eCFR by keyword.

```
GET https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/search-regulations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eCFR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/search-regulations?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/search-regulations?${params}`, {
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
| `query` | string | yes | Search query text, such as agriculture. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `order` | list | no | Optional result ordering: relevance, citations, hierarchy, newest_first, oldest_first, or suggestions. One of: `0`, `1`, `2`, `3`, `4`, `5`. |
| `perPage` | number | no | Maximum number of search results to return per page. |
| `page` | number | no | One-based search results page number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {},
      "results": [
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
| `meta` | object | Search pagination and summary metadata. |
| `results` | array<object> | Matching regulation search results. |

## Native endpoint

Through the native eCFR API, this operation is `GET /api/search/v1/results` (base URL `https://www.ecfr.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-regulations.md) for the provider-specific parameters and requirements.

