# Nightfall.ai: Search Violations

Finds violations in Nightfall.ai by search filters.

```
GET https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/search-violations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nightfall.ai `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/search-violations?connectionId=$CONNECTION_ID&limit=25&offset=0&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/search-violations?${params}`, {
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
| `query` | string | yes | Nightfall search query string, for example state:pending. |
| `sort` | list | no | Optional sort order such as TIME_DESC, TIME_ASC, RELEVANCE, RISK_ASC, or RISK_DESC. One of: `Relevance`, `Risk Asc`, `Risk Desc`, `Time Asc`, `Time Desc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "violations": [
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
| `violations` | array<object> | Violation results matching the supplied Nightfall query. |

## Native endpoint

Through the native Nightfall.ai API, this operation is `GET /dlp/v1/violations/search` (base URL `https://api.nightfall.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-violations.md) for the provider-specific parameters and requirements.

