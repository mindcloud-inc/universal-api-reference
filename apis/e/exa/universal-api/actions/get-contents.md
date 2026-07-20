# Exa: Get Contents

Retrieves page contents from Exa.

```
GET https://connect.mindcloud.co/v1/universal/exa/latest/actions/get-contents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exa/latest/actions/get-contents?connectionId=$CONNECTION_ID&urls%5B%5D=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "urls[]": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exa/latest/actions/get-contents?${params}`, {
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
| `urls[]` | array<string> | yes | Array of URLs to crawl (backwards compatible with 'ids' parameter). |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ids[]` | array<string> | no | Deprecated - use 'urls' instead. Array of document IDs obtained from searches. |
| `text.maxCharacters` | number | no | Maximum character limit for the full page text. Useful for controlling response size and API costs. |
| `text.includeHtmlTags` | boolean | no | Include HTML tags in the response, which can help LLMs understand text structure and formatting. Default: `false`. |
| `highlights.numSentences` | number | no | The number of sentences to return for each snippet. |
| `highlights.highlightsPerUrl` | number | no | The number of snippets to return for each result. |
| `highlights.query` | string | no | Custom query to direct the LLM's selection of highlights. |
| `summary` | object | no | Summary of the webpage |
| `livecrawl` | string | no | Options for livecrawling pages. 'never': Disable livecrawling (default for neural search). 'fallback': Livecrawl when cache is empty. 'always': Always livecrawl. 'preferred': Always try to livecrawl, but fall back to cache if crawling fails. |
| `livecrawlTimeout` | number | no | The timeout for livecrawling in milliseconds. Default: `10000`. |
| `maxAgeHours` | number | no | Maximum age of cached content in hours. Controls when livecrawling is triggered based on content freshness. - Positive value (e.g. 24): Use cached content if it's less than this many hours old, otherwise livecrawl. - 0: Always livecrawl, never use cache. - -1: Never livecrawl, always use cache. - Omit (default): Livecrawl as fallback only when no cached content exists. |
| `subpages` | number | no | The number of subpages to crawl. The actual number crawled may be limited by system constraints. Default: `0`. |
| `subpageTarget` | string | no |  |
| `extras.links` | number | no | Number of URLs to return from each webpage. Default: `0`. |
| `extras.imageLinks` | number | no | Number of images to return for each result. Default: `0`. |
| `context.maxCharacters` | number | no | Maximum character limit. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "entities": [
        {}
      ],
      "extras": {},
      "favicon": "string",
      "highlights": [
        "string"
      ],
      "highlightScores": [
        1
      ],
      "id": "string",
      "image": "string",
      "publishedDate": "2026-05-07T12:00:00.000Z",
      "score": 1,
      "subpages": [
        {}
      ],
      "summary": "string",
      "text": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `entities` | array<object> |  |
| `extras` | object |  |
| `favicon` | string |  |
| `highlights` | array<string> |  |
| `highlightScores` | array<number> |  |
| `id` | string |  |
| `image` | string |  |
| `publishedDate` | date |  |
| `score` | number |  |
| `subpages` | array<object> |  |
| `summary` | string |  |
| `text` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Exa API, this operation is `POST /contents` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contents.md) for the provider-specific parameters and requirements.

