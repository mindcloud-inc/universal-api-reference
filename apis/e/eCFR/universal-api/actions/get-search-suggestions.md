# eCFR: Get Search Suggestions

Retrieves search suggestions for a query from eCFR.

```
GET https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/get-search-suggestions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eCFR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/get-search-suggestions?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/get-search-suggestions?${params}`, {
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
| `query` | string | yes | Partial search text for suggestions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "suggestions": [
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
| `suggestions` | array<object> | Suggested search completions. |

## Native endpoint

Through the native eCFR API, this operation is `GET /api/search/v1/suggestions` (base URL `https://www.ecfr.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-search-suggestions.md) for the provider-specific parameters and requirements.

