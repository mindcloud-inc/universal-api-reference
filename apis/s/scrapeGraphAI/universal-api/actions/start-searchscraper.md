# ScrapeGraphAI: Start SearchScraper

Starts a SearchScraper search job in ScrapeGraphAI.

```
POST https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/start-searchscraper
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeGraphAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/start-searchscraper" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userPrompt": "What is ScrapeGraphAI and what does it do?"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/start-searchscraper', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userPrompt": "What is ScrapeGraphAI and what does it do?"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userPrompt` | string | yes | Search query or question to answer. Example: `What is ScrapeGraphAI and what does it do?`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `headers` | object | no | Optional custom headers for the search request. Example: `[object Object]`. |
| `mock` | boolean | no | Return mock data instead of performing a live search. Default: `false`. |
| `outputSchema` | object | no | Optional schema object to structure search results. Example: `[object Object]`. |
| `stealth` | boolean | no | Enable stealth mode to bypass bot protection. Default: `false`. |
| `timeRange` | string | no | Filter results by recency. Example: `past_week`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "markdownContent": "string",
      "numResults": 1,
      "referenceUrls": [
        "https://example.com"
      ],
      "requestId": "string",
      "result": {},
      "status": "string",
      "userPrompt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string | Error message when the request fails. |
| `markdownContent` | string | Markdown content when returned by the service. |
| `numResults` | number | Number of results returned. |
| `referenceUrls` | array<string> | Reference URLs used for the answer. |
| `requestId` | string | Unique identifier for the SearchScraper request. |
| `result` | object | Structured search result payload. |
| `status` | string | Current status of the request. |
| `userPrompt` | string | Original search prompt. |

## Native endpoint

Through the native ScrapeGraphAI API, this operation is `POST /searchscraper` (base URL `https://api.scrapegraphai.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-searchscraper.md) for the provider-specific parameters and requirements.

