# Exa: Find Similar Links

Finds links similar to a URL in Exa.

```
GET https://connect.mindcloud.co/v1/universal/exa/latest/actions/find-similar-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exa/latest/actions/find-similar-links?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exa/latest/actions/find-similar-links?${params}`, {
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
| `url` | string | yes | The url for which you would like to find similar links. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `numResults` | number | no | Number of results to return (up to thousands of results available for custom plans) Default: `10`. |
| `includeDomains[]` | array<string> | no | List of domains to include in the search. If specified, results will only come from these domains. |
| `excludeDomains[]` | array<string> | no | List of domains to exclude from search results. If specified, no results will be returned from these domains. |
| `startCrawlDate` | date | no | Crawl date refers to the date that Exa discovered a link. Results will include links that were crawled after this date. Must be specified in ISO 8601 format. |
| `endCrawlDate` | date | no | Crawl date refers to the date that Exa discovered a link. Results will include links that were crawled before this date. Must be specified in ISO 8601 format. |
| `startPublishedDate` | date | no | Only links with a published date after this will be returned. Must be specified in ISO 8601 format. |
| `endPublishedDate` | date | no | Only links with a published date before this will be returned. Must be specified in ISO 8601 format. |
| `includeText[]` | array<string> | no | List of strings that must be present in webpage text of results. Currently, only 1 string is supported, of up to 5 words. |
| `excludeText[]` | array<string> | no | List of strings that must not be present in webpage text of results. Currently, only 1 string is supported, of up to 5 words. Checks from the first 1000 words of the webpage text. |
| `context.maxCharacters` | number | no | Maximum character limit. |
| `contents` | object | no |  |

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

Through the native Exa API, this operation is `POST /findSimilar` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-similar-links.md) for the provider-specific parameters and requirements.

