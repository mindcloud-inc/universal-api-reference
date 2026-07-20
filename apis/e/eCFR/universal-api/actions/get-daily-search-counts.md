# eCFR: Get Daily Search Counts

Retrieves daily search result counts from eCFR.

```
GET https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/get-daily-search-counts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eCFR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/get-daily-search-counts?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/get-daily-search-counts?${params}`, {
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
| `query` | string | yes | Search query text for daily counts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dates": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dates` | object | Search match counts keyed by date. |

## Native endpoint

Through the native eCFR API, this operation is `GET /api/search/v1/counts/daily` (base URL `https://www.ecfr.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-daily-search-counts.md) for the provider-specific parameters and requirements.

