# eCFR: Summarize Search Results

Retrieves summary details for search results from eCFR.

```
GET https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/summarize-search-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eCFR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/summarize-search-results?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/summarize-search-results?${params}`, {
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
| `query` | string | yes | Search query text to summarize. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object | Search result summary metadata. |

## Native endpoint

Through the native eCFR API, this operation is `GET /api/search/v1/summary` (base URL `https://www.ecfr.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/summarize-search-results.md) for the provider-specific parameters and requirements.

