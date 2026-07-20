# Perplexity: Search the Web

Finds web search results in Perplexity by query.

```
GET https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/search-the-web
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perplexity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/search-the-web?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/search-the-web?${params}`, {
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
| `query` | string | yes | Search query. Perplexity also accepts an array of queries; this action currently models the common single-query path. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `country` | string | no | ISO 3166-1 alpha-2 country code for geographically relevant results. |
| `maxResults` | number | no | Maximum number of results to return (1-20). |
| `maxTokens` | number | no | Maximum total tokens of webpage content to return across results. |
| `maxTokensPerPage` | number | no | Maximum tokens extracted from each webpage. |
| `searchLanguageFilter[]` | array<string> | no | ISO 639-1 language codes to filter search results. |
| `searchDomainFilter[]` | array<string> | no | Allowlist or denylist of domains to search. |
| `lastUpdatedAfterFilter` | string | no | Return results updated after this date (MM/DD/YYYY). |
| `lastUpdatedBeforeFilter` | string | no | Return results updated before this date (MM/DD/YYYY). |
| `searchAfterDateFilter` | string | no | Return results published after this date (MM/DD/YYYY). |
| `searchBeforeDateFilter` | string | no | Return results published before this date (MM/DD/YYYY). |
| `searchRecencyFilter` | string | no | Publication recency filter: hour, day, week, month, or year. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "results": [
        {
          "date": "string",
          "last_updated": "string",
          "snippet": "string",
          "title": "string",
          "url": "https://example.com"
        }
      ],
      "server_time": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `results[].date` | string |  |
| `results[].last_updated` | string |  |
| `results[].snippet` | string |  |
| `results[].title` | string |  |
| `results[].url` | string |  |
| `server_time` | string |  |

## Native endpoint

Through the native Perplexity API, this operation is `POST /search` (base URL `https://api.perplexity.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-the-web.md) for the provider-specific parameters and requirements.

